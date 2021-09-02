<script>
    import PercentageDisplay from "../PercentageDisplay.svelte";
    import { Link } from "svelte-routing";
</script>

<div class="page-section half-page-section">
    <div class="section-content">
        <h3 class="upper">Putting our health and planet first</h3>
        <p class="section-content-text">
            Refour is more than packaging. We are the greenest solution on the
            planet, paving a path towards a better future. With the lowest cost
            and the best performing features, we put a sustainable material into
            reach of all corporations that want to act now to help restore and
            renew our planet. We are not paper, nor plastic, and we do not mix
            materials. We are 100% recyclable.
        </p>
        <Link class="full-width" to="material">
            <p class=" section-content-text section-content-cta">
                READ MORE
                <img src="assets/CTA-arrow.svg" alt="arrow" />
            </p>
        </Link>
    </div>
    <div class="section-content">
        <PercentageDisplay percent={100} title="Recyclable" />
        <PercentageDisplay percent={80} title="Lower carbon footprint" />
        <PercentageDisplay percent={60} title="Lower cost" />
        <PercentageDisplay percent={50} title="Less material-user" />
    </div>
</div>

<style>
    .section-content {
        width: 40%;
    }
    .upper {
        text-transform: uppercase;
    }
    .section-content-text {
        width: 100%;
    }
    p {
        font-size: 18px;
        margin-bottom: 40px;
    }
    .section-content-cta {
        font-weight: bold;
    }
    .section-content :global(.full-width) {
        width: 100%;
    }
    h3 {
        font-size: 30px;
        margin-bottom: 15px;
    }
    .section-content-text > img {
        margin-left: 12px;
    }
    @media only screen and (max-width: 1110px) {
        .half-page-section {
            flex-direction: column-reverse;
        }
    }
    .section-content {
        width: 100%;
    }
</style>
