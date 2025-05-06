<script>
    import { writable } from 'svelte/store';
    import { fade, slide } from 'svelte/transition';

    let isDropDownOpen = writable(false);

    function toggleDropDown(){
        isDropDownOpen.update(value => !value);
    }
</script>




<header class="bg-slate-800 fixed w-full z-20">


  <nav class="bg-slate-800">
    <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
    <a href="/" class="flex items-center space-x-3 rtl:space-x-reverse">
        <img src="/Logo.png" class="h-8" alt="Flowbite Logo" />
        <span class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white">NicKnowsCode</span>
    </a>
    <div class="flex md:order-2 space-x-3 md:space-x-0 rtl:space-x-reverse">
      <a href="https://docs.google.com/document/d/1RmAHWgXpGa6JorTw2g1Zic7fmsIcyKixj-e0dW-0Do8/edit?usp=sharing" target="_blank" class="hidden md:block">
        <button type="button" class="text-white bg-slate-800 hover:bg-gray-500 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg px-4 py-2 text-center hover:text-slate-950">Résumé <span aria-hidden="true">→</span></button>
      </a>
        <button data-collapse-toggle="navbar-cta" type="button" on:click={toggleDropDown} class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600" aria-controls="navbar-cta" aria-expanded="false">
          <span class="sr-only">Open main menu</span>
          <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
        </svg>
      </button>
    </div>
    <div class="items-center justify-between hidden w-full md:flex md:w-auto md:order-1" id="navbar-cta">
      <ul class="flex flex-col font-medium p-12 text-center  md:p-0 mt-4 border border-gray-100 rounded-lg bg-slate-800 md:space-x-8 rtl:space-x-reverse md:flex-row md:mt-0 md:border-0 ">
        <li>
          
          <a href="/info" class="block py-2 px-3 md:p-0 text-white rounded transition-transform duration-150 hover:scale-125 md:hover:bg-transparent">Info</a>
          
        </li>
        <li>
          <a href="/works" class="block py-2 px-3 md:p-0 text-white rounded transition-transform duration-150 hover:scale-125 md:hover:bg-transparent">Works</a>
          
        </li>
        <li>
          <a href="/contact" class="block py-2 px-3 md:p-0 text-white rounded transition-transform duration-150 hover:scale-125 md:hover:bg-transparent ">Contact</a>
        </li>
      </ul>
    </div>
    </div>
  </nav>
  



    <div class="absolute -bottom-11 left-0 w-full overflow-hidden leading-[0]">
        <svg class="relative block w-[calc(100%+1.3px)] h-[44px] rotate-y-180" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
          <path d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z " style="fill: #1e293b;"></path>
        </svg>
    </div>






    <!-- Mobile menu, show/hide based on menu open state. -->
     {#if $isDropDownOpen}
    <div class="lg:hidden" role="dialog" aria-modal="true">
      <!-- Background backdrop, show/hide based on slide-over state. -->
      <div class="fixed inset-0 z-10"></div>
      <div class="fixed inset-y-0 right-0 z-10 w-full overflow-y-auto bg-slate-950 px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
        <div class="flex items-center justify-between">
          <a href="/" class="-m-1.5 p-1.5">
            <span class="sr-only">Your Company</span>
            <img class="h-8 w-auto" src="/Logo.png" alt="">
          </a>
          <button type="button" on:click={toggleDropDown} class="-m-2.5 rounded-md p-2.5 text-slate-400">
            <span class="sr-only">Close menu</span>
            <svg class="size-6" fill="none" viewBox="0 0 24 24" stroke-width="3" stroke="currentColor" aria-hidden="true" data-slot="icon">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
            </svg>
            
          </button>
        </div>
        <div class="mt-6 flow-root">
          <div class="-my-6 divide-y divide-gray-500/10">
            <div class="space-y-2 py-6">

              <a href="/info" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-slate-400 hover:bg-slate-400 hover:text-slate-950">info</a>
              <a href="/works" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-slate-400 hover:bg-slate-400 hover:text-slate-950">works</a>
              <a href="/contact" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-slate-400 hover:bg-slate-400 hover:text-slate-950">contact</a>
            </div>
            <div class="py-6">
              <a href="https://docs.google.com/document/d/1RmAHWgXpGa6JorTw2g1Zic7fmsIcyKixj-e0dW-0Do8/edit?usp=sharing" target="_blank" class="-mx-3 block rounded-lg px-3 py-2.5 text-base/7 font-semibold text-slate-400 hover:bg-slate-400 hover:text-slate-950">Resume</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    {/if}
</header>