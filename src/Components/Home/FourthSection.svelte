<script>
    import Card from "../Card.svelte";

    let cardContents = [
        {
            title: "Sustainability",
            link: "sustainability",
            text: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.",
            imageName: "card-1.png",
        },
        {
            title: "Material",
            link: "material",
            text: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.",
            imageName: "card-2.png",
        },
        {
            title: "End Application",
            link: "endApp",
            text: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.",
            imageName: "card-1.png",
        },
        {
            title: "Cost",
            link: "cost",
            text: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.",
            imageName: "card-2.png",
        },
    ];
</script>

<div class="page-section full-page-section">
    {#each cardContents as card}
        <Card props={card} />
    {/each}
</div>
<hr />
<div class="page-section half-page-section">
    <img src="assets/icon_quote.svg" alt="quote" />
    <div class="quote-container">
        <h2>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin diam
            purus, lacinia vitae tortor ut, mollis tincidunt urna.
        </h2>
    </div>
    <div class="author-container">
        <hr />
        Kildens Navn
    </div>
</div>

<style>
    .full-page-section {
        flex-wrap: wrap;
    }
    hr {
        border: 2px dashed #4040411a;
        border-style: none none dashed;
        color: var(--bg-color);
        background-color: var(--bg-color);
    }
    .half-page-section {
        flex-direction: column;
        justify-content: center;
    }
    .half-page-section > img {
        height: 85px;
        width: 85px;
    }

    .quote-container {
        margin: 30px 0px;
        width: 60%;
        text-align: center;
    }

    .author-container {
        align-items: center;
    }
    .author-container > hr {
        width: 15px;
        height: 1px;
        border: 1px solid var(--accent-color);
        margin-right: 5px;
    }
    @media only screen and (max-width: 1110px) {
        .full-page-section {
            justify-content: space-evenly;
        }
        .quote-container {
            width: 100%;
            margin: 15px 0;
        }
    }
</style>
