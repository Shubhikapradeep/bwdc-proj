<script>
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <img class="home-img" src="Debtinc.png" alt="A chart that compares median home value to median home income ratio " />
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                <strong>
                     In reality, Debt Often Outpaces Assets

                </strong>
                In many southern states, Black median debt is nearly as high as total assets.
                Some even have negative net worth for the median household — meaning debts outweigh assets.

            </ArticleText>

            <ArticleText> Interpretation: wealth-building is structurally blocked, and not solvable by education alone.
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
