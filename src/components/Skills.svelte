<script lang="ts">
  import { onMount } from 'svelte';

  // Dynamically import all images from a folder
  const images = [
    { id: 1, src: '/icons/aws.png', alt: 'Random Image 1' },
    { id: 2, src: '/icons/c-sharp.png', alt: 'Random Image 2' },
    { id: 3, src: '/icons/css-3.png', alt: 'Random Image 3' },
    { id: 4, src: '/icons/database.png', alt: 'Random Image 4' },
    { id: 5, src: '/icons/html-5.png', alt: 'Random Image 5' },
    { id: 6, src: '/icons/javascript.png', alt: 'Random Image 6' },
    { id: 7, src: '/icons/js.png', alt: 'Random Image 7' },
    { id: 8, src: '/icons/python.png', alt: 'Random Image 8' },
    { id: 9, src: '/icons/unity.png', alt: 'Random Image 9' },
    { id: 10, src: '/icons/wordpress.png', alt: 'Random Image 10' },
    { id: 11, src: '/icons/unreal.png', alt: 'Random Image 11' }
  ];

  let container: HTMLElement | null = null;


  let imagesData = images.map((image) => {
  // Determine screen size
  const screenWidth = getScreenWidth();

  let x;
  if (screenWidth < 640) {
    // Small screens
    x = Math.random() * 150;
  } else if (screenWidth >= 640 && screenWidth < 1280) {
    // Medium screens
    x = Math.random() * 400;
  } else {
    // Large screens
    x = Math.random() * 700;
  }

  let y;
  if (screenWidth < 640) {
    // Small screens
    y = Math.random() * 300;
  } else {y = Math.random() * 150;}

  return {
    ...image,
    x, // Dynamic X position
    y, // Dynamic Y position
    dx: (Math.random() - 0.5) * 0.25, // Random horizontal speed
    dy: (Math.random() - 0.5) * 0.25  // Random vertical speed
  };
});


  function getScreenWidth() {
    if (typeof window !== 'undefined') {
      return window.innerWidth;
    }
    return 1024; // Default width for server-side rendering
  }


  const animate = () => {
    if (!container) return;

    const containerRect = container.getBoundingClientRect();

    // Update each image's position
    imagesData = imagesData.map((image) => {
      let { x, y, dx, dy } = image;

      // Update position
      x += dx;
      y += dy;

      // Bounce off walls
      if (x <= 0 || x + 50 >= containerRect.width) {
        dx *= -1; // Reverse horizontal direction
      }
      if (y <= 0 || y + 50 >= containerRect.height) {
        dy *= -1; // Reverse vertical direction
      }

      return { ...image, x, y, dx, dy };
    });

    requestAnimationFrame(animate); // Loop the animation
  };

  onMount(() => {
    animate(); // Start the animation
  });
</script>

  <!-- <div class="mt-32 relative flex items-center justify-center pb-10" >
      <hr class="absolute w-[60%] lg:mx-96 md:mx-56 sm:mx-32 border-t border-slate-700" />
      <div class="relative bg-slate-950 px-4 text-slate-700 text-sm font-bold" id="aboutme" >My Toolbox
        </div>
  </div> -->


  <div bind:this={container} class="relative mx-auto w-[50%] h-[350px] sm:h-[250px] bg-slate-950 overflow-visible border border-slate-700 rounded-md  mb-16">
    <div 
      class="absolute -top-3 left-1/2 transform -translate-x-1/2 bg-slate-950 px-4 text-white text-sm font-bold"
      id="aboutme">
      My Toolbox
  </div>
{#each imagesData as image (image.id)}
  <img
    src={image.src}
    alt={image.alt}
    class="absolute w-12 h-12 bg-slate-700 rounded-full p-1"
    style="transform: translate({image.x}px, {image.y}px);"
  />
{/each}
</div>

  


