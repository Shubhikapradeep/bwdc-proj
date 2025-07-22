<script>
    let { children } = $props();
</script>

<div class="article-text">
    <p>
        {@render children()}
    </p>
</div>

<style>
    .article-text {
        margin: 50vh auto;
        width: 50%;
        font-size: 26px;
        background-color: #ddcc77;
        color: #117733;
        border: solid #aa4499 3px;
        border-radius: 20px;
        padding: 20px;
        box-shadow: 16px 16px #f67e4b;
    }
</style>
