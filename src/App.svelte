<script>
  import AppHeader from "./components/app/AppHeader.svelte";
  import Home from './pages/home.svelte'
  import List from './pages/list.svelte'
  import AppContainer from "./components/app/AppContainer.svelte";
  import Router from 'svelte-spa-router'
  import AppFooter from "./components/app/AppFooter.svelte";

  const routes = {
    '/': Home,
    '/list': List
  }

</script>

<style>
  .bg-color {
    height: 600px;
  }
  .wrapper {
    min-height: 100vh;
  }
</style>

<div class="wrapper">
  <div class="relative bg-color w-full bg-indigo-400">
    <div class="absolute bottom-0 left-0 w-full transform rotate-180 z-0">
      <img alt="img" src="/images/liner.svg">
    </div>
    <AppHeader/>
    <AppContainer>
      <Router routes="{routes}"/>
    </AppContainer>
  </div>
  <AppFooter/>
</div>

