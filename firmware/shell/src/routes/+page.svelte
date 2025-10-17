<script lang="ts">
    import { invoke } from "@tauri-apps/api/core";
    import Main from "./components/Main.svelte";
    import Statusbar from "./components/Statusbar.svelte";

    let imageSource = "/cat.png";
</script>

<main class="container">
    <img
        class="bg"
        src={imageSource}
        alt="there was an error while displaying the background"
    />
    <div class="stack">
        <Statusbar /><br />
        <Main />
    </div>
</main>

<style>
    @import url("https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap");

    :root {
        font-family: Inter, sans-serif;
        font-size: 16px;
        line-height: 24px;
        font-weight: 400;

        color: white;
        background-color: black;

        font-synthesis: none;
        text-rendering: optimizeLegibility;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        -webkit-text-size-adjust: 100%;
        height: 240px;
        overflow: hidden;
    }
    .stack {
        --margin: 7px;

        display: flex;
        flex-direction: column;
        top: var(--margin);
        bottom: var(--margin);
        left: var(--margin);
        width: 160px;
    }
    .bg {
        position: fixed;
        top: 0;
        left: 0;
        width: 110%;
        height: 110%;
        object-fit: cover;
        z-index: -1;
        filter: blur(3px) brightness(75%);
    }

    .container {
        margin: 0;
        padding-top: 10vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style>
