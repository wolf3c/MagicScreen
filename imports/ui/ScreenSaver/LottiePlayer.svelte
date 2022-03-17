<script>
    // from: https://github.com/LottieFiles/lottie-player
    // find lottie file at https://lottiefiles.com/
    import "@lottiefiles/lottie-player";

    export let src = "https://assets4.lottiefiles.com/packages/lf20_0xbu1xfo.json";
    export let style = "width: 320px";
</script>

<div class="lottie-container center">
    <lottie-player
        autoplay
        loop
        mode="normal"
        src={src}
        style={style}
    />
</div>

<style>
    .lottie-container {
        width: 100%;
        height: 100%;
    }
</style>
