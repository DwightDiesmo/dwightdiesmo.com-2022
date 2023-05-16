<script>
  import svelteLogo from './assets/svelte.svg'
  import Contact from './lib/Contact.svelte';
  import Counter from './lib/Counter.svelte'
  import Footer from './lib/Footer.svelte';
  import Navbar from './lib/Navbar.svelte';
  import Projects from './lib/Projects.svelte';
  import Publications from './lib/Publications.svelte';
  import Resume from './lib/Resume.svelte';
  import Terminal from './lib/Terminal.svelte';
</script>

<main>
  <Navbar />
  <Publications />
  <Terminal />
  <Resume />
  <Projects />
  <Contact />
  <Footer />
</main>
