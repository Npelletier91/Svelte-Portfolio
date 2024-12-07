<script>
  import ContactForm from "../../components/ContactForm.svelte";
  import Header from "../../components/Header.svelte";


</script>
  

<div>
    <Header/>
    <div class="pt-40"></div> 
    <div class="flex flex-wrap md:flex-nowrap gap-4 px-4">


            <!-- Section 1: Placeholder for Another Component -->
            <div class="bg-slate-800 px-10 py-24 my-32 mx-14 rounded-lg shadow-md flex flex-col justify-between h-full order-2 md:order-1">

              <p class=" text-slate-50 lg:text-3xl text-2xl font-semibold text-center pb-2">Have questions? Email me:</p>
              <div class="pb-48">
                <a href="mailto:nicolas-pelletier@outlook.com" class="text-slate-400 underline lg:text-xl text-lg">
                  nicolas-pelletier@outlook.com
                </a>
              </div>


              <p class=" text-slate-50 lg:text-3xl text-2xl font-semibold text-center pb-4">Socials</p>
              <div class="grid gap-6 grid-cols-2 lg:grid-cols-4 place-items-center">

                <a href="https://github.com/Npelletier91" target="_blank">
                    <img src="/GitHub.png" alt="GitHub Logo" class="social-icon">
                </a>
                <a href="https://nicolaspelletier.itch.io/" target="_blank">
                    <img src="/itch.png" alt="Itch.io Logo" class="social-icon">
                </a>
                <a href="https://www.linkedin.com/in/nicolas-pelletier-ab0b6a268" target="_blank">
                    <img src="/Linkedin.jpg" alt="LinkedIn Logo" class="social-icon">
                </a>
                <a href="https://docs.google.com/document/d/1fBlrtccNKqebRN0xyxNKS_Hvl76OHp8zRUOkWw-5rt8/edit?usp=sharing" target="_blank">
                    <img src="/Resume.jpg" alt="Resume Icon" class="social-icon">
                </a>
              </div>
            </div>


      <!-- Section 2: ContactForm -->
      <div class="flex-1 order-1 md:order-2">
        <ContactForm />
      </div>
  

    </div>
</div>
