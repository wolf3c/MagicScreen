<script>
    import Fire from "./Fire.svelte";
</script>

<div class="container">
    <div class="fire"><Fire /></div>
    <div class="fire"><Fire /></div>
    <div class="fire"><Fire /></div>
    <div class="fire"><Fire /></div>
    <div class="fire"><Fire /></div>
    <div class="fire"><Fire /></div>
    <div class="fire"><Fire /></div>
    <div class="fire"><Fire /></div>
    <div class="fire"><Fire /></div>
    <div class="fire"><Fire /></div>
    <div class="fire"><Fire /></div>
    <div class="fire"><Fire /></div>
</div>

<style>
    .container {
        display: flex;
        width: 100%;
        height: 100vh;

        display: flex;
        /* gap: 16px; */

        justify-content: center;
        align-items: flex-end;
    }
    .fire {
        position: relative;
        bottom: -100px;
    }
</style>
