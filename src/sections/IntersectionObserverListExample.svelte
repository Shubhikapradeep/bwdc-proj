<script>
    import { blur, slide } from "svelte/transition";
    import Scroller from "../lib/Scroller.svelte";
    import ObservedArticleText from "../lib/ObservedArticleText.svelte";
    import ArticleText from "../lib/ArticleText.svelte";

    const options = {
        threshold: [0.95],
    };

    const callback = (entries, observer) => {
        entries.forEach((entry) => {
            const elem = entry.target;
            // TODO: only do this if we're scrolling upward
            if (entry.intersectionRatio >= 0.9) {
                // "active" state
                elem.style.backgroundColor = "#ddcc77";
                if (firstList.length > 0) {
                const listItem = firstList.pop();
                secondList.push(listItem);
            }
            }
        });
    };

    let firstList = $state([
        "Assets",
        "Homeownership",
        "Debts",
        "Access to education",
        "Access to Credit(SBA 7a and 504 Loans)",
        "Percent Population of Black people in state",
        "Number of Biz formations and firms",
    ]);

    let secondList = $state([]);
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <div id="lists-container">
                <div class="list">
                    <h3> Hypothesis : Factors that affect Black Business Ownership</h3>
                    {#each firstList as item}
                        <div
                            class="list-item"
                            in:slide={{ duration: 750 }}
                            out:blur={{ duration: 1000 }}
                        >
                            {item}
                        </div>
                    {/each}
                </div>

                <div class="list">
                    <h3>Actual Results</h3>
                    {#each secondList as item}
                        <div
                            class="list-item"
                            in:slide={{ duration: 750 }}
                            out:blur={{ duration: 1000 }}
                        >
                            {item}
                        </div>
                    {/each}
                </div>
            </div>
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
            Bee's Conclusion : So what really affected the increase in black business ownership - indicator wise?
            </ArticleText>

            <ObservedArticleText {callback} {options}>
                Number of firms and formations, help somewhat in gathering receipts and whether these businesses are in profit, but can't directly contribute to an increase in wealth.
            </ObservedArticleText>

            <ObservedArticleText {callback} {options}>
             They give an idea of the potentially self employed Black people in a state, but no further indication.
            </ObservedArticleText>

            <ObservedArticleText {callback} {options}>
                Actually a solid indicator, but alas - turns out its a better indicator for the increase in attainment of bachelor's degrees rather than black owned businesses. Better luck next time? :)
            </ObservedArticleText>

            <ObservedArticleText {callback} {options}>
                Access to education, was not a direct indicator and thus distracted us from the true factors contributing to our hypothesis.
            </ObservedArticleText>

            <ObservedArticleText {callback} {options}>
                Debts give another very good idea about whether these businesses are profitable and are contributing to their wealth.
            </ObservedArticleText>

            <ObservedArticleText {callback} {options}>
                Homes are the most likely to be used as collateral, so intuitively and functionally - they are the best indicators so far(at least in my knowledge).
            </ObservedArticleText>

            <ObservedArticleText {callback} {options}>
                Assets, once again contribute to the wealth directly and can act as collateral thus suplementing and directly acting as a good indicator.
            </ObservedArticleText>
            <ObservedArticleText {callback} {options}>
                These factor don't stop here, it just builds up and still further widens the wealth gap. 
            </ObservedArticleText>
            <ObservedArticleText {callback} {options}>
                Which is why these stories are shared, I hope this creates an impact on you :)
            </ObservedArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    #lists-container {
        display: flex;
        position: fixed;
        flex: 1 1; /* Allows growing, shrinking */
        width: 100%;
    }

    .list {
        margin: 0px 20px;
        background-color: #cc6677;
        color: #aa4477;
        border: solid #aa4477 3px;
        border-radius: 20px;
        font-size: 16px;
        box-shadow: 16px 16px #4477aa;
        width: 100%;
    }

    .list-item {
        background-color: #ddcc77;
        color: #aa4477;
        border: solid #aa4477 3px;
        border-radius: 20px;
        padding: 10px;
        font-size: 16px;
        width: 50%;
        margin: 5px auto;
        text-align: center;
    }

    h3 {
        text-align: center;
        font-size: 26px;
    }
</style>
