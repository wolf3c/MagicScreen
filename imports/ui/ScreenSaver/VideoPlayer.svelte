<script>
    export let src = null;
</script>

<video src={src} autoplay loop muted></video>

<style>
    video {
        width: 100%;
        max-height: 100%;
        position: fixed;
        bottom: 0;
    }
</style>