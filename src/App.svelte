<script>
  import data from './assets/portfolio'; // 
  import {Router, Route, Link} from'svelte-routing';
  import Title from './lib/components/Title.svelte';
  import Portfolio from './lib/components/Portfolio.svelte';
  import About from './lib/components/About.svelte';
  import Detail from './lib/components/Detail.svelte';

  let title = 'Hello,<br> I\'m Doolee';
  export let url = '';
</script>

<Router {url}>
  <nav>
    <Link to="/">home</Link>
    <Link to="/portfolio">portfolio</Link>
    <Link to="/about">about</Link>
  </nav>

  <div>
    <Route path="/" component={Title} {title} />
    <Route path="/portfolio" component={Portfolio} {data} />
    <Route path="/about" component={About} />
    <Route path="/detail/:id" component={Detail} {data} />
  </div>
</Router>
