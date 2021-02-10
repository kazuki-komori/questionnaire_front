<script>
  import AppCard from "../components/app/AppCard.svelte";
    let hoge = ""
</script>
<div>
    <div class="py-10">
        <AppCard>
            <textarea {hoge} class="w-full border-4 border-indigo-400 p-2 text-2xl" placeholder="質問を入力する" name="q" id="q" cols="20" rows="5"></textarea>
        </AppCard>
    </div>
    <div>
        <button
                class="block mx-auto px-3 py-1 shadow-2xl rounded bg-white text-indigo-400 text-2xl font-semibold hover:opacity-75"
        >
            質問する
        </button>
    </div>
</div>