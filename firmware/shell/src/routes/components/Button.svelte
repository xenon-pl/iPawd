<script lang="ts">
    import { onMount } from "svelte";

    console.log("ts pmo!!!");

    export let text = "undefined";
    export let onclick = undefined;
    export let classes = "";
</script>

<button class="button {classes}" on:click={onclick}>{text}</button>

<style>
    .button {
        --margin: 7px;

        font-family: Inter, sans-serif;

        width: 140px;
        height: 30px;
        background: rgba(64, 64, 64, 0.78);
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
