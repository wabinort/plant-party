<script>
    export let name = "Plant name";
    export let genus = "Lorem Ipsum";
    export let photo = "";
    export let reference = "https://google.com";
</script>

<a href="{reference}">
    <article class="card">
        <img src="{photo}" alt="{name} image">
        <div>
            <h2>{name}</h2>
            <small>{genus}</small>
        </div>
    </article>
</a>

<style>
    a {
        color: initial;
        transition: 500ms;
        transition-delay: 300ms;

    }
    a:hover {
        text-decoration: underline;
    }
    article {
        max-width: 60rem;
        background-color: rgb(224, 236, 203);
        border-radius: 15px;
    }

    .card {
        display: flex;
        height: 300px;
        margin: 1rem;
        position: relative;
        width: 300px;
        box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);
    }

    .card:hover {
        box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
    }

    img {
        width: 33%;
    }

    small {
        font-style: italic;
    }
</style>