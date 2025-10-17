<script lang="ts">
    import Button from "./Button.svelte";

    console.log("ts pmo!!!");
</script>

<div class="menu">
    <Button text="Music" classes="selected" />
    <Button text="Playlists" />
</div>

<style>
    .menu {
        background: rgba(43, 43, 43, 0.9);
        backdrop-filter: blur(15px);
        border-radius: 22px;
        overflow: hidden;
        padding-top: 9px;
        height: 197px;
        margin-top: 7px;
    }
</style>
