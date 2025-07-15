<!-- svelte-ignore css_unused_selector -->
<script>
    export let image;
    export let title;
    export let description;
</script>

<div class="card">
    <img src={image} alt={title} />
    <div class="card-content">
        <h2 class="card-title">{title}</h2>
        <p class="card-description">{description}</p>
    </div>
</div>

<style>
    .card {
        background-color: #35b5ac;
        border: 1px solid #ddd;
        border-radius: 10px;
        overflow: hidden;
        width: 300px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        margin: 20px;
        text-align: center;
        justify-content: center;
        margin-left: 28%;
        font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
            "Lucida Sans", Arial, sans-serif;
    }

    .card img {
        width: 100%;
        height: auto;
    }

    .card-content {
        padding: 15px;
        font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
            "Lucida Sans", Arial, sans-serif;
    }

    .card-title {
        font-size: 1.5em;
        margin: 0 0 10px 0;
        font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
            "Lucida Sans", Arial, sans-serif;
    }

    .card-description {
        font-size: 1em;
        color: #666;
        margin: 0;
        font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
            "Lucida Sans", Arial, sans-serif;
    }
    body {
        background-color: #35b5ac;
    }
</style>
