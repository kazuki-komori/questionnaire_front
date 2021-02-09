<script>
  import AppContainer from "./AppContainer.svelte";
  import AppCard from "./AppCard.svelte";
</script>
<style>
    .custom-shape-divider-bottom-1612872436 .shape-fill {
        fill: white;
    }
</style>
<div class="relative py-10">
    <AppCard>
        <nav class="grid grid-cols-2 text-indigo-400 text-2xl text-center font-semibold tracking-wide px-6">
            <p>質問する</p>
            <p>過去の回答</p>
        </nav>
    </AppCard>
    <div class="px-10 pt-8">
        <AppContainer>
            <p class="text-3xl font-medium text-white">質問する</p>
        </AppContainer>
    </div>
</div>