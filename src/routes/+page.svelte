<script>
    import ContactForm from "../components/ContactForm.svelte";
    import Description from "../components/Description.svelte";
    import Footer from "../components/Footer.svelte";
    import Header from "../components/Header.svelte";
    import Main from "../components/Main.svelte"
    import Skills from "../components/Skills.svelte";4
    import FadeInOnScroll from "../components/FadeInOnScroll.svelte";
</script>


<div>
    <Header />
    <Main />
    <FadeInOnScroll>
      <Description />
    </FadeInOnScroll>
    <FadeInOnScroll>
      <Skills />
    </FadeInOnScroll>
    <FadeInOnScroll threshold={.3}>
      <ContactForm />
    </FadeInOnScroll>
    <Footer />
  </div>
