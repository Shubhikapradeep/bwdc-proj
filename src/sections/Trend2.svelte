<script>
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <img class="home-img" src="homeown.png" alt="A chart that compares median home value to median home income ratio " />
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                <strong>
                     Higher Homeownership Doesn’t Always Mean More Wealth
                </strong>
                States with high Black homeownership (like South Carolina or Georgia) don’t always show higher net worth.
                In contrast, some states with lower homeownership still show better assets (e.g., Illinois).
            </ArticleText>

            <ArticleText> Interpretation: Homeownership is necessary but not sufficient — alone, it doesn't actually close the wealth gap.
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
