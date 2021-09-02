<script>
    import { Link } from "svelte-routing";
    export let props = {
        imageName: "",
        title: "",
        text: "",
        link: "",
    };
    let hovered = false;
</script>

<div
    class="card-container"
    on:mouseenter={() => {
        hovered = true;
    }}
    on:mouseleave={() => {
        hovered = false;
    }}
>
    <img src="assets/{props.imageName}" alt="card" />
    <div class="card-content {hovered ? 'card-content-hovered' : ''}">
        <div class="title-row">
            <span class="title">{props.title}</span>
            <img src="assets/CTA-arrow.svg" alt="arrow" />
        </div>

        <span class="content">{props.text}</span>
    </div>
</div>

<style>
    .card-container {
        min-height: 420px;
        width: 20%;
        min-width: 250px;
        flex-direction: column;
        align-items: center;
        transition: 0.3s;
        cursor: pointer;
        margin: 20px;
    }

    .card-container:hover {
        margin-bottom: 24px;
    }
    .card-container > img {
        width: 100%;
        height: 200px;
        object-fit: cover;
        border-radius: 20px 20px 0px 0px;
    }
    .card-content {
        flex-direction: column;
        border: 2px dashed #70707033;
        border-top: none;
        border-radius: 0 0 20px 20px;
    }
    .card-content-hovered {
        background-color: #ffffff99;
        box-shadow: 0px 8px 25px #0000000d;
    }
    .title-row {
        width: 100%;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        padding: 25px 25px 0 25px;
    }
    .title {
        font-weight: 700;
        font-size: 1.5vw;
    }
    .content {
        padding: 25px;
    }
    @media only screen and (max-width: 1110px) {
        .title {
            font-size: 20px;
        }
    }
</style>
