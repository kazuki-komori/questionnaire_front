<script>
  import {push} from 'svelte-spa-router'
  import AppContainer from "./AppContainer.svelte";
  import AppCard from "./AppCard.svelte";
  let ActiveTab = "home"
  const handleClick = (tab) => {
    if (!tab) {
      return
    }
    if (tab === "home") {
      push('/')
      ActiveTab = "home"
    }
    if (tab === "list") {
      push('/list')
      ActiveTab = "list"
    }
  }
</script>
<div class="relative py-8">
    <AppCard>
        <nav class="grid grid-cols-2 text-gray-600 text-2xl text-center font-semibold tracking-wide px-6">
            <p class="{ActiveTab === 'home' ? 'text-indigo-400 border-b-2 border-indigo-400' : ''}" on:click={() => handleClick('home')}>質問する</p>
            <p class="{ActiveTab === 'list' ? 'text-indigo-400 border-b-2 border-indigo-400' : ''}" on:click={() => handleClick('list')}>過去の回答</p>
        </nav>
    </AppCard>
    <div class="pt-8">
        <AppContainer>
            <p class="text-center text-2xl font-medium text-white">かずやんの質問箱</p>
            <div class="pt-6 flex items-center justify-center">
                <span class="rounded shadow-md bg-gray-800 py-2 px-3 text-center text-white font-semibold mr-3">
                    <a href="https://github.com/kazuki-komori" target="_blank">
                        GitHub
                    </a>
                </span>
                <span class="rounded shadow-md bg-blue-400 py-2 px-3 text-center text-white font-semibold">
                    <a href="https://twitter.com/D_kazuyan" target="_blank">
                        Twitter
                    </a>
                </span>
            </div>
        </AppContainer>
    </div>
</div>