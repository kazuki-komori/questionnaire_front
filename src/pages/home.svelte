<script>
  import AppCard from "../components/app/AppCard.svelte";
    const hoge = () => {
      console.log("hoge")
    }
</script>
<div>
    <AppCard>
        <textarea class="w-full border-4 border-indigo-400 p-2 text-2xl" name="q" id="q" cols="20" rows="5"></textarea>
    </AppCard>
</div>