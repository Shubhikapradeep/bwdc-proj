<script>
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <img class="home-img" src="SBA.png" alt="A chart that compares median home value to median home income ratio " />
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                <strong>
                     Receipts per Firm Correlate More with Assets than Education
                </strong>
                In states with higher net worth, Black-owned businesses generally show higher average receipts.
But high-education states (like Massachusetts or Connecticut) don’t always reflect strong business performance.

            </ArticleText>

            <ArticleText> Interpretation: So really, Capital access + asset security matter more than formal credentials as seen here in this graph for SBA and 504 loan applications.
.
.
</ArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    .home-img {
        width: 100%;
        margin: 0px auto;
    }
</style>
