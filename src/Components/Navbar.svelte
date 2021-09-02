<script>
    import { Router, Route, Link } from "svelte-routing";

    let showUnderlining = new Array(7).fill(false);
    let mobileNavShowing = false;
</script>

<div class="content-container">
    <Link to="/"><img src="assets/logo.png" alt="logo" /></Link>
    <div
        class="mobile-nav"
        on:click={() => {
            mobileNavShowing = !mobileNavShowing;
        }}
    >
        {#if !mobileNavShowing}
            <img src="assets/burger.svg" alt="burger" />
        {:else}
            <img src="assets/cross.svg" alt="cross" />
        {/if}
    </div>
    <div class="nav-container">
        <Link to="sustainability">
            <div
                class="nav-item"
                on:mouseenter={() => {
                    showUnderlining[0] = !showUnderlining[0];
                }}
                on:mouseleave={() => {
                    showUnderlining[0] = !showUnderlining[0];
                }}
            >
                Sustainability
                <hr
                    class="underlining {showUnderlining[0]
                        ? 'underlining-show'
                        : ''}"
                />
            </div>
        </Link>

        <Link to="material">
            <div
                class="nav-item"
                on:mouseenter={() => {
                    showUnderlining[1] = !showUnderlining[1];
                }}
                on:mouseleave={() => {
                    showUnderlining[1] = !showUnderlining[1];
                }}
            >
                Material
                <hr
                    class="underlining {showUnderlining[1]
                        ? 'underlining-show'
                        : ''}"
                />
            </div></Link
        >

        <Link to="endapp">
            <div
                class="nav-item"
                on:mouseenter={() => {
                    showUnderlining[2] = !showUnderlining[2];
                }}
                on:mouseleave={() => {
                    showUnderlining[2] = !showUnderlining[2];
                }}
            >
                End application
                <hr
                    class="underlining {showUnderlining[2]
                        ? 'underlining-show'
                        : ''}"
                />
            </div></Link
        >

        <Link to="cost">
            <div
                class="nav-item"
                on:mouseenter={() => {
                    showUnderlining[3] = !showUnderlining[3];
                }}
                on:mouseleave={() => {
                    showUnderlining[3] = !showUnderlining[3];
                }}
            >
                Cost
                <hr
                    class="underlining {showUnderlining[3]
                        ? 'underlining-show'
                        : ''}"
                />
            </div></Link
        >

        <Link to="about">
            <div
                class="nav-item"
                on:mouseenter={() => {
                    showUnderlining[4] = !showUnderlining[4];
                }}
                on:mouseleave={() => {
                    showUnderlining[4] = !showUnderlining[4];
                }}
            >
                About
                <hr
                    class="underlining {showUnderlining[4]
                        ? 'underlining-show'
                        : ''}"
                />
            </div></Link
        >

        <Link to="faq">
            <div
                class="nav-item"
                on:mouseenter={() => {
                    showUnderlining[5] = !showUnderlining[5];
                }}
                on:mouseleave={() => {
                    showUnderlining[5] = !showUnderlining[5];
                }}
            >
                FAQ
                <hr
                    class="underlining {showUnderlining[5]
                        ? 'underlining-show'
                        : ''}"
                />
            </div></Link
        >

        <Link to="contact">
            <div
                class="nav-item"
                on:mouseenter={() => {
                    showUnderlining[6] = !showUnderlining[6];
                }}
                on:mouseleave={() => {
                    showUnderlining[6] = !showUnderlining[6];
                }}
            >
                Contact
                <hr
                    class="underlining {showUnderlining[6]
                        ? 'underlining-show'
                        : ''}"
                />
            </div>
        </Link>
    </div>
</div>
<div class="mobile-nav-container {mobileNavShowing ? '' : 'hidden'}">
    <Link to="sustainability">
        <div class="nav-item">Sustainability</div>
    </Link>
    <Link to="material">
        <div class="nav-item">Material</div></Link
    >
    <Link to="endapp">
        <div class="nav-item">End application</div></Link
    >
    <Link to="cost">
        <div class="nav-item">Cost</div></Link
    >
    <Link to="about">
        <div class="nav-item">About</div></Link
    >
    <Link to="faq">
        <div class="nav-item">FAQ</div></Link
    >
    <Link to="contact">
        <div class="nav-item">Contact</div>
    </Link>
</div>

<style>
    .content-container {
        position: fixed;
        z-index: 10;
        top: 0;
        left: 0;
        width: 100vw;
        height: var(--navbar-height);

        background-color: white;
        box-shadow: 0px 0px 15px #00000012;
        padding: 35px 60px;

        flex-direction: row;
        align-items: center;
        justify-content: space-between;
    }

    .nav-item {
        transition: 0.3s;
        margin-left: 50px;
        font-size: 16px;
        display: flex;
        flex-direction: column-reverse;

        align-items: center;
    }
    .nav-item:hover {
        /* font-weight: bold; */
        text-shadow: -0.08ex 0 var(--text-color), 0.08ex 0 var(--text-color);
    }
    .underlining {
        transition: 0.3s;
        position: absolute;
        top: 35px;
        width: 0px;
        border: none;
        border-top: 2px dashed var(--accent-color);
    }
    .underlining-show {
        width: 35px;
    }
    .mobile-nav {
        display: none;
    }
    .mobile-nav-container {
        display: none;
    }
    .hidden {
        z-index: -1 !important;
    }
    @media only screen and (max-width: 1110px) {
        .nav-container {
            display: none;
        }
        .mobile-nav {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 40px;
            width: 40px;
            border-radius: 3px;

            cursor: pointer;
            border: 1.5px dashed var(--accent-color);
        }
        .mobile-nav > img {
            height: 30px;
            width: 30px;
        }
        .content-container {
            padding: 20px;
        }
        .mobile-nav-container {
            z-index: 9;
            position: fixed;
            top: var(--navbar-height);
            width: 100%;
            display: flex;
            flex-direction: column;
            box-shadow: 0px 0px 15px #00000022;
        }
        .nav-item {
            width: 100%;
            height: 50px;
            align-items: center;
            justify-content: center;
            background-color: var(--bg-color);
            font-weight: bold;
            border-bottom: 1.5px dashed var(--accent-color);
            margin-left: 0;
        }
    }
</style>
