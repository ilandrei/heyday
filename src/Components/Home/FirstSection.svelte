<script>
    import { Link } from "svelte-routing";
    import * as animateScroll from "svelte-scrollto";
</script>

<div class="page-section full-page-section first-section">
    <div class="section-content">
        <h1>
            <span class="accent">REINVENTING</span>
        </h1>
        <br />
        <h1>PACKAGING</h1>
        <p class="section-content-text">
            Introducing the most sustainable material category for packaging on
            the market, with the lowest costs and carbon footprint to date
        </p>
        <Link class="full-width" to="sustainability">
            <p class=" section-content-text section-content-cta">
                READ MORE
                <img src="assets/CTA-arrow.svg" alt="arrow" />
            </p>
        </Link>
    </div>

    <div class="section-content">
        <img src="assets/bin-temp.png" alt="generic bin" />
    </div>
    <div class="section-anchor" on:click={() => animateScroll.scrollToBottom()}>
        <img
            src="assets/arrow-down.svg"
            alt="arrow-down"
            class="floating-img"
        />
    </div>
</div>

<style>
    .first-section {
        padding-top: var(--navbar-height);
    }

    .section-content-text {
        width: 100%;

        font-size: 18px;
        margin-top: 40px;
    }
    .section-content-text > img {
        margin-left: 12px;
    }
    .section-content-text {
        width: 100%;
    }
    .section-content-cta {
        font-weight: bold;
    }
    .section-content :global(.full-width) {
        width: 100%;
    }
    .section-content > img {
        height: 60vh;
        width: auto;
        object-fit: contain;
    }
    .section-anchor {
        position: absolute;
        bottom: 60px;
        left: 50%;
        transform: translateX(-50%);
    }
    .section-anchor > .floating-img {
        padding: 15px;
    }
    .section-anchor > .floating-img:hover {
        padding: 20px;
    }
    .section-content {
        width: 40%;
    }
    @media only screen and (max-width: 800px) {
        h1 {
            font-size: 10vw;
            line-height: 40px;
        }
        .section-content > img {
            margin-top: 20px;
            height: 30vh;
            width: auto;
            object-fit: contain;
        }
    }
    @media only screen and (max-width: 1110px) {
        .section-anchor {
            bottom: 20px;
        }
        .full-page-section {
            flex-direction: column;
        }
        .section-content {
            width: 100%;
        }
        .first-section {
            height: 80vh;
        }
        .section-content:nth-child(2) {
            align-items: center;
            justify-content: flex-start;
        }

        br {
            height: 0px;
        }
    }
</style>
