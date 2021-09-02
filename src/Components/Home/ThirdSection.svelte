<script>
    let playHovered = false;
    let width = 0;
</script>

<svelte:window bind:innerWidth={width} />

<div class="page-section {width > 1000 ? 'full' : 'half'}-page-section">
    <div class="player-container">
        <img src="assets/video-placeholder.png" alt="video" class="player" />
        <div
            class="play-border-container {playHovered
                ? 'play-border-hovered'
                : ''}"
        >
            <div
                class="play-button-container"
                on:mouseenter={() => {
                    playHovered = true;
                }}
                on:mouseleave={() => {
                    playHovered = false;
                }}
            >
                <img src="assets/icon-play.svg" alt="play" />
            </div>
        </div>
    </div>
</div>

<div class="page-section half-page-section">
    <img src="assets/gif-placeholder.png" alt="gif-logo" />
</div>

<style>
    .player-container {
        width: 100%;

        border: 2px dashed var(--accent-color);
        border-radius: 40px;
        padding: 25px;
    }
    .player-container > img {
        object-fit: conver;
        width: 100%;
        height: auto;
    }
    .play-border-container {
        position: absolute;

        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);

        height: 80px;
        width: 80px;
        border-radius: 50%;

        align-items: center;
        justify-content: center;
        cursor: pointer;
        transition: 0.2s;
        border: 1px dotted var(--accent-color);
    }
    .play-button-container:hover {
        height: 80px;
        width: 80px;
        background-color: #f26b3c;
    }
    .play-button-container {
        position: absolute;
        transition: 0.3s;
        height: 90px;
        width: 90px;
        border-radius: 50%;
        background-color: var(--accent-color);
        align-items: center;
        justify-content: center;
    }
    .play-border-hovered {
        height: 90px;
        width: 90px;
        border: 1.5px dashed var(--accent-color);
    }
    .half-page-section {
        align-items: center;
        justify-content: center;
    }
    .half-page-section > img {
        width: 40%;
        height: auto;
    }
    @media only screen and (max-width: 1110px) {
        .half-page-section {
            min-height: 30vh;
        }
        .half-page-section > img {
            width: 60%;
        }
        .player-container {
            border-radius: 10px;
            padding: 10px;
        }
    }
</style>
