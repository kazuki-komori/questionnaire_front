<script>
  const world = 'postcss'; // edit world and save to see hmr update
  import Hello from './pages/hello.svelte'
  import page from 'page'
  let component = ''
  page('/hello', () => component = Hello)
  page()
</script>

<style>
  h1 {
    color: orangered; /* change color an save to see hmr update */
    /* you can also use css nesting
    & .world {
      font-size: 2rem;
    }
    */
  }
  .world {
    @apply text-green-500 italic; /*  here's some tailwind apply */
  }
</style>

<h1 class="border border-current rounded p-4 m-4">
  <!-- tailwind classes in svelte template -->
  Hello
<!--  <span class="world">{world}</span>-->
<!--  <Hello hello="hoge" />-->
  <svelte:component this="{component}"/>
</h1>

