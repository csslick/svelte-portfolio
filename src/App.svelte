<script>
  import Title from './lib/components/Title.svelte';
  import Portfolio from './lib/components/Portfolio.svelte';
  import About from './lib/components/About.svelte';

  let title = 'Hello,<br> I\'m Doolee';
</script>

<nav>
  <a href="#home">home</a>
  <a href="#portfolio">portfolio</a>
</nav>
<Title {title} />
<Portfolio />
<About />



