<script>
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <img class="duck-img" src="receipts.png" alt="Receipts per firm graph!" />
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                <strong>
                     Receipts per Black-Owned Firm Vary Wildly!
                </strong>
                Some states have many firms but very low receipts — e.g., Mississippi or Alabama.
Others (like New York or California) have fewer firms but much higher receipts per firm.
            </ArticleText>

            <ArticleText> Interpretation: It’s not about how many Black businesses exist — it’s about the conditions they operate in (access to capital, urban markets, etc.).
</ArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    .duck-img {
        width: 100%;
        margin: 0px auto;
    }
</style>
