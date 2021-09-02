<script>
    import { onMount } from "svelte";

    export let title = "";
    export let percent = 0;

    let auxPercent = 0;
    onMount(() => {
        animateWidth();
    });
    const animateWidth = async () => {
        while (auxPercent < percent) {
            await timeout(20);
            auxPercent++;
        }
    };
    const timeout = (ms) => new Promise((resolve) => setTimeout(resolve, ms));
</script>

<div class="component-container">
    <div class="title-row">
        <span class="title">{title}</span><span class="percent">{percent}%</span
        >
    </div>
    <div class="progress-bar">
        <div class="progress-bar-fill" style="width:{auxPercent}%;" />
    </div>
</div>

<style>
    .component-container {
        flex-direction: column;
        width: 100%;
        margin: 20px 0;
    }
    .title-row {
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 12px;

        font-weight: 600;
        font-size: 16px;
    }
    .title {
        opacity: 50%;
    }
    .progress-bar {
        width: 100%;
        height: 5px;
        border-radius: 3px;
        background-color: rgba(64, 64, 65, 0.1);
    }
    .progress-bar-fill {
        background-color: var(--accent-color);
        height: 100%;
        border-radius: 3px;
        transition: 0.5s;
    }
</style>
