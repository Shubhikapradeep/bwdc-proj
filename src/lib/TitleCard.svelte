<script>
    let { title, subtitle } = $props();
</script>

<div class="title-card">
    <div class="content">
        <h1>{title}</h1>
        <p>{subtitle}</p>
    </div>
</div>

<style>
    .title-card {
        background-color: #117733;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 2rem;
        box-sizing: border-box;
        font-family: "Inter", sans-serif;
        font-size: 26px;
    }

    .content {
        max-width: 700px;
        background-color: #117733;
        padding: 2rem;
        border: 6px solid #ddcc77;
        border-radius: 2rem;
        box-shadow: 16px 16px #117733;
        font-size: 26px;
    }

    h1 {
        font-size: 3rem;
        margin: 0;
        color: #ddcc77;
        text-shadow: 1px 1px 0 #117733;
        font-size: 50px;
    }

    p {
        font-size: 1.3rem;
        color: #f7f5eb;
        margin-top: 1rem;
        font-size: 26px;
    }

    @media (max-width: 600px) {
        h1 {
            font-size: 2.2rem;
        }

        p {
            font-size: 1.1rem;
        }
    }
</style>
