<script lang="ts">
    import { onMount } from "svelte";

    console.log("ts pmo!!!");

    export let text = "undefined";
    export let onclick = undefined;
</script>

<div class="statusbar">{text}</div>

<style>
    .statusbar {
        --margin: 7px;

        position: absolute;
        font-family: Inter, sans-serif;
        top: var(--margin);
        width: 160px;
        height: 30px;
        background: rgba(43, 43, 43, 0.9);
        backdrop-filter: blur(15px);
        border-radius: 48px;
        overflow: hidden;
        border: 0;
        margin-bottom: 7px;
        color: white;
        text-align: left;
    }
    .selected {
        background: rgba(255, 255, 255, 0.76);
        color: rgb(0, 0, 0);
        font-weight: 400;
    }
</style>
