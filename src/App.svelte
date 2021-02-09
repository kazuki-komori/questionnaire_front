<script>
  import AppHeader from "./components/app/AppHeader.svelte";
  import Home from './pages/home.svelte'
  import page from 'page'
  import AppContainer from "./components/app/AppContainer.svelte";

  let component = ''
  page('/', () => component = Home)
  page()
</script>

<style>
</style>

<div>
  <div class="relative h-96 w-full bg-indigo-400">
    <div class="absolute bottom-0 left-0 w-full transform rotate-180 z-0">
      <img alt="img" src="/images/liner.svg">
    </div>
    <AppHeader/>
    <AppContainer>
      <svelte:component this="{component}"/>
    </AppContainer>
  </div>
</div>

