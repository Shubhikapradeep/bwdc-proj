<script>
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";
</script>
<div>
    <Scroller layout="left">
        {#snippet sticky()}
            <div>
                <p>
                    So, how did I decide to research on this project?
                </p>
                <p>
                    <strong
                        > Swipe up to see!</strong
                    >
                </p>
            </div>
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                First : I decided to look through all datasets and do a basic exploratory data analysis on the 16 directly related to my data.
            </ArticleText>

            <ArticleText>
               Second : After performing an EDA, I started getting a clear direction of where I was headed - some trends were so visible in the data, that I just had to try telling their story :)
            </ArticleText>

            <ArticleText>
                Third : I started developing a basic idea, and story telling workflow for it
            </ArticleText>

            <ArticleText>
                <strong>
                    Fourth : The most important part - feedback from my BWDC mentors David and Parth, who helped guide me and narrow my problem statement to be viable and easy to approach
                </strong>
            </ArticleText>
            <ArticleText>
                <strong>
                    Let me share some of these trends with you!
                </strong>
            </ArticleText>
        {/snippet}
    </Scroller>
</div>
<style>
  .hypothesis {
    margin: 2rem 0;
    text-align: center;
    max-width: 700px;
     font-size: 1.125rem;
    line-height: 1.5;
    color: #333;
  }
  .hypothesis img {
    max-width: 100%;
    height: auto;
    border-radius: 12px;
    margin-bottom: 1rem;
  }
</style>
