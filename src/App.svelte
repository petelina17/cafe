<script>
  import logo from './assets/svelte.png'
  import './lib/TailwindCSS.svelte'
  import Footer from './components/Footer.svelte'
  import TopBanner from './components/TopBanner.svelte'
  import Header from './components/Header.svelte'
  import Home from './pages/Home.svelte'
  import Products from './pages/Products.svelte'
  import Page404 from './Page404.svelte'
  import Router from 'svelte-spa-router'


  const routes = {
    '/': Home,
    '/products': Products,
    '*': Page404
  }

</script>

<main class="text-offblack flex flex-col min-h-screen">
  <TopBanner/>
  <Header/>
  <div class="flex-grow" style="min-height:1400px">
        <Router {routes} restoreScrollState={true} />
  </div>

  <div>

    <Footer/>
  </div>

</main>
<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
    Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    text-align: center;
    margin: 0 auto;
  }

  img {
    height: 16rem;
    width: 16rem;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 1rem auto;
    line-height: 1.35;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
</style>
