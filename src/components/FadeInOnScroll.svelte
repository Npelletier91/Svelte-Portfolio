<script lang="ts">
    import { onMount } from 'svelte';
  
    export let threshold: number = 0.2; 
    export let duration: number = 1500; 
  
    let isVisible: boolean = false;
    let element: HTMLElement | null = null;
  
    onMount(() => {
      const observer = new IntersectionObserver(
        (entries) => {
          if (entries[0].isIntersecting) {
            isVisible = true; 
            observer.disconnect(); // Stop observing once visible
          }
        },
        { threshold }
      );
  
      if (element) {
        observer.observe(element); // Attach observer to the element
      }
  
      return () => observer.disconnect(); // Cleanup observer
    });
  </script>
  
  <div
    bind:this={element}
    class="transition-opacity duration-[var(--fade-duration)] opacity-0"
    style="opacity: {isVisible ? 1 : 0}; --fade-duration: {duration}ms;"
  >
    <slot />
  </div>
  