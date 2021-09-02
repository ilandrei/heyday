<script>
    import { fade } from "svelte/transition";
    import FirstSection from "../Components/Home/FirstSection.svelte";
    import FourthSection from "../Components/Home/FourthSection.svelte";
    import SecondSection from "../Components/Home/SecondSection.svelte";
    import ThirdSection from "../Components/Home/ThirdSection.svelte";
    import Footer from "../Components/Footer.svelte";
    import FifthSection from "../Components/Home/FifthSection.svelte";
    let floatingShowing = false;
</script>

<svelte:head>
    <title>Refour Home</title>
</svelte:head>
<div
    class="floating-action-container"
    on:mouseenter={() => {
        floatingShowing = true;
    }}
    on:mouseleave={() => {
        floatingShowing = false;
    }}
>
    {#if floatingShowing}
        <div transition:fade class="floating-content-container">
            <div class="floating-container-row">
                <p><span class="accent">Lorem</span>&nbsp; ipsum dolar sit</p>
            </div>
            <div class="floating-container-row floating-section-title">
                <img src="assets/icon-leaf.png" alt="leaf" />
                <span>Trees cut down this year</span>
            </div>
            <div class="floating-container-row floating-big-row">
                152.124.156
            </div>
            <div class="floating-container-row floating-section-title">
                <img src="assets/icon-co2.png" alt="co2" />
                <span>CO2 emissions this year</span>
            </div>
            <div class="floating-container-row floating-big-row">
                254.241.245
            </div>
        </div>
    {/if}

    <img src="assets/icon-earth.svg" alt="earth" class="floating-img " />
</div>
<div class="page-container">
    <FirstSection />
    <SecondSection />
    <ThirdSection />
    <FourthSection />
    <FifthSection />
    <Footer />
</div>

<style>
    .floating-action-container {
        position: fixed;
        bottom: 60px;
        right: 40px;

        z-index: 2;
    }

    .floating-content-container {
        position: absolute;
        height: 330px;
        width: 350px;
        top: -260px;
        left: -370px;

        margin-right: 20px;
        padding: 40px 35px;

        background-color: #fcfbf9;
        border-radius: 10px;
        border: 2px dashed #70707033;

        flex-direction: column;
    }
    .floating-container-row {
        font-weight: bold;
        font-size: 18px;

        flex-direction: row;
        align-items: center;
    }
    .floating-container-row > img:nth-child(1) {
        width: 24px;
        margin-right: 5px;
    }
    .floating-container-row > img:nth-child(2) {
        width: 32px;
        margin-right: 5px;
    }
    .floating-section-title {
        margin-top: 30px;
    }
    .floating-section-title > span {
        opacity: 50%;
    }
    .floating-big-row {
        font-size: 40px;
        font-weight: 700;
    }
    .page-container {
        display: flex;
        flex-direction: column;
    }
    @media only screen and (max-width: 1110px) {
        .floating-action-container {
            bottom: 20px;
            right: 10px;
        }
        .floating-content-container {
            height: 330px;
            width: 350px;
            top: -340px;
            left: -280px;
            /* transform: translateX(100); */
        }
    }
</style>
