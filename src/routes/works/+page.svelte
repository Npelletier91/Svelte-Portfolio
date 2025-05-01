<script>
    import Header from "../../components/Header.svelte";
  
  </script>
  
  
  <div>
      <Header />
      <div class="bg-slate-950 py-24 sm:py-32">
        <div class="mx-auto max-w-2xl px-6 lg:max-w-7xl lg:px-8">
          <h2 class="text-center text-base/7 font-extrabold text-slate-700">My Work</h2>
          <p class="mx-auto mt-2 max-w-lg text-center text-4xl font-extrabold tracking-tight text-balance text-white sm:text-5xl">Past and Current Projects</p>
          <div class="mt-10 grid gap-4 sm:mt-16 lg:grid-cols-3 lg:grid-rows-2">


            <div class="relative lg:row-span-2 hover:scale-[1.02] transition-transform cursor-pointer">
                <a href="https://nicolaspelletier.itch.io/hangover-hero" class="block">
                <div class="absolute inset-px rounded-lg bg-slate-800 lg:rounded-l-[2rem]"></div>
                <div class="relative flex h-full flex-col overflow-hidden rounded-[calc(var(--radius-lg)+1px)] lg:rounded-l-[calc(2rem+1px)]">
                    <div class="px-8 pt-8 pb-3 sm:px-10 sm:pt-10 sm:pb-0">
                    <p class="mt-2 text-xl font-extrabold tracking-tight text-white max-lg:text-center">Hangover Hero</p>
                    <p class="mt-2 max-w-lg text-sm/6 text-gray-400 max-lg:text-center">A mobile game developed with Unity using over 100 C# scripts. Hangover Hero will be deployed for Andriod and iPhone.</p>
                    </div>
                    <div class="@container relative min-h-[38rem] w-full grow max-lg:mx-auto max-lg:max-w-sm">
                        <div class="absolute inset-x-8 top-10 bottom-0 overflow-hidden flex items-center justify-center rounded-t-[4cqw] border-x-[1cqw] border-t-[2cqw] border-slate-950 bg-slate-950 shadow-2xl">
                        <img class="max-h-none object-cover rotate-90 scale-[1.8] translate-y-8" src="\HangoverHero.png" alt="">
                        </div>
                    </div>
                </div>
                </a>
                <div class="pointer-events-none absolute inset-px rounded-lg shadow-sm ring-1 ring-black/5 lg:rounded-l-[2rem]"></div>
            </div>




            <div class="relative max-lg:row-start-1 hover:scale-[1.02] transition-transform cursor-pointer">
                <a href="https://github.com/Npelletier91/BlazorPortfolioApp?tab=readme-ov-file" class="block">
              <div class="absolute inset-px rounded-lg bg-slate-800 max-lg:rounded-t-[2rem]"></div>
              <div class="relative flex h-full flex-col overflow-hidden rounded-[calc(var(--radius-lg)+1px)] max-lg:rounded-t-[calc(2rem+1px)]">
                <div class="px-8 pt-8 sm:px-10 sm:pt-10">
                  <p class="mt-2 text-xl font-extrabold tracking-tight text-white max-lg:text-center">Blazor Web Applications</p>
                  <p class="mt-2 max-w-lg text-sm/6 text-gray-400 max-lg:text-center">Flash Card application and a Daily Recipe app using Blazor.</p>
                </div>
                <div class="flex flex-1 items-center verflow-hidden justify-center px-8 max-lg:pt-10 max-lg:pb-12 sm:px-10 lg:pb-2">
                  <img class="w-full max-lg:max-w-xs  rounded-t-[1cqw] scale-[0.9]" src="/FlashCardApp.png" alt="">
                </div>
              </div>
            </a>
              <div class="pointer-events-none absolute inset-px rounded-lg shadow-sm ring-1 ring-black/5 max-lg:rounded-t-[2rem]"></div>
            </div>
            


            <div class="relative max-lg:row-start-3 lg:col-start-2 lg:row-start-2 hover:scale-[1.02] transition-transform cursor-pointer">
                <a href="https://github.com/Npelletier91/Castle-Conquest" class="block">
              <div class="absolute inset-px rounded-lg bg-slate-800"></div>
              <div class="relative flex h-full flex-col overflow-hidden rounded-[calc(var(--radius-lg)+1px)]">
                <div class="px-8 pt-8 sm:px-10 sm:pt-10">
                  <p class="mt-2 text-xl font-extrabold tracking-tight text-white max-lg:text-center">Castle Couquest</p>
                  <p class="mt-2 max-w-lg text-sm/6 text-gray-400 max-lg:text-center">Castle Conquest is a 2D platform runner game developed in C# using Unity.</p>
                </div>
                <div class="@container flex flex-1 items-center max-lg:py-6 lg:pb-2">
                  <img class="w-full max-lg:max-w-xs  rounded-t-[1cqw] scale-[.9]" src="\CastleConquest.png" alt="">
                </div>
              </div>
              </a>
              <div class="pointer-events-none absolute inset-px rounded-lg shadow-sm ring-1 ring-black/5"></div>
            </div>



            <div class="relative lg:row-span-2 hover:scale-[1.02] transition-transform cursor-pointer">
                <a href="https://github.com/Npelletier91/Svelte-Portfolio" class="block">
              <div class="absolute inset-px rounded-lg bg-slate-800 max-lg:rounded-b-[2rem] lg:rounded-r-[2rem]"></div>
              <div class="relative flex h-full flex-col overflow-hidden rounded-[calc(var(--radius-lg)+1px)] max-lg:rounded-b-[calc(2rem+1px)] lg:rounded-r-[calc(2rem+1px)]">
                <div class="px-8 pt-8 pb-3 sm:px-10 sm:pt-10 sm:pb-0">
                  <p class="mt-2 text-xl font-extrabold tracking-tight text-white max-lg:text-center">Portfolio Website</p>
                  <p class="mt-2 max-w-lg text-sm/6 text-gray-400 max-lg:text-center">This site is entirely built using Svelte and TailwindCSS</p>
                </div>
                <div class="relative min-h-[30rem] w-full grow">
                    <div class="relative mx-10 mt-10 rounded-tl-xl bg-gray-900 shadow-2xl overflow-auto">                        
                    <div class="flex bg-gray-800/40 ring-1 ring-white/5">
                      <div class="-mb-px flex text-sm/6 font-medium text-gray-400">
                        <div class="border-r border-b border-r-white/10 border-b-white/20 bg-white/5 px-4 py-2 text-white">Main.svelte</div>
                        <div class="border-r border-gray-600/10 px-4 py-2">+page.svelte</div>
                      </div>
                    </div>
                <div class="relative mx-10 mt-5 max-h-[32rem] overflow-hidden rounded-tl-xl bg-gray-900 shadow-2xl">
                <pre class="bg-gray-900 text-white break-words text-left">
{`const animate = () => {
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
                            `}
                        </pre>
                    </div>
                    
                  </div>
                </div>
              </div>
              </a>
              <div class="pointer-events-none absolute inset-px rounded-lg shadow-sm ring-5 ring-black/5 max-lg:rounded-b-[2rem] lg:rounded-r-[2rem]"></div>
            </div>
          </div>
        </div>
      </div>
        
  </div>