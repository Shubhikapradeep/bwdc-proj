<script>
    import * as Highcharts from "highcharts";
    import "highcharts/modules/exporting";
    import { Chart } from "@highcharts/svelte";
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";

    let options = {
        chart: {
            type: "pie",
        },
        title: {
            text: "An Example Pie Chart",
        },
        plotOptions: {
            pie: {
                allowPointSelect: true,
                dataLabels: [
                    {
                        enabled: true,
                        distance: 20,
                    },
                    {
                        enabled: true,
                        distance: -40,
                        format: "{point.percentage:.1f}%",
                        style: {
                            fontSize: "1.2em",
                            textOutline: "none",
                        },
                        filter: {
                            operator: ">",
                            property: "percentage",
                            value: 10,
                        },
                    },
                ],
            },
        },
        series: [
            {
                name: "Group",
                data: [
                    {
                        name: "Group 1",
                        y: 151,
                    },
                    {
                        name: "Group 2",
                        sliced: true,
                        selected: true,
                        y: 180,
                    },
                    {
                        name: "Group 3",
                        y: 32,
                    },
                    {
                        name: "Group 4",
                        y: 103,
                    },
                    {
                        name: "Group 5",
                        y: 77,
                    },
                ],
            },
        ],
    };
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
        <img class="bw-img" src="bwinfographic.png" alt="Infographic that explores different factors contributing to black wealth" />
    
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                <strong>Hi, my name is Bee, and I'm really glad to meet you 
                </strong>
                    Welcome to my Scrollytelling session!
            </ArticleText>

            <ArticleText>
                My hypothesis to test for this project came up while exploring the BWDC site and data on Business Ownership and Employment
            </ArticleText>

            <ArticleText>
                 This made me curious about how encouraging education and increasing availability of credit could influence more self-employment
                <br /><br />
            </ArticleText>

            <ArticleText>
                <strong>
                    thus potentially increasing wealth among Black individuals and impacting State Wealth.

                </strong>
            </ArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    .bw-img {
        width: 90%;
        margin: 0px auto;
    }
</style>