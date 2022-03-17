<script>
    import Fires from "./Fires.svelte";
    import VideoPlayer from "./VideoPlayer.svelte";
    import LottiePlayer from "./LottiePlayer.svelte";

    const data = [
        {
            _id: "0",
            name: "fire",
            type: "video",
            src: "/videos/fire.mp4",
        },{
            _id: "1",
            name: "plant",
            type: "lottie",
            src: "/lottie/99260-succulent-plant-animation.json",
        },{
            _id: "2",
            name: "bicycle",
            type: "lottie",
            src: "/lottie/98267-bicycle.json",
        }, {
            _id: "3",
            name: "stroller",
            type: "lottie",
            src: "/lottie/7098-roll-it-retro-stroller.json",
        }, {
            _id: "4",
            name: "horse",
            type: "lottie",
            src: "/lottie/7096-roll-it-rocking-horse.json",
        }, {
            _id: "5",
            name: "hot-tea",
            type: "lottie",
            src: "/lottie/99331-hot-tea.json",
        }, {
            _id: "6",
            name: "moon",
            type: "lottie",
            src: "/lottie/93809-moon.json",
        }
    ]

    const type2modal = {
        video: VideoPlayer,
        lottie: LottiePlayer
    }

    let a = data[0];
    a.modal = type2modal[a.type]
</script>

<div class="container">
    <svelte:component this={a.modal} src={a.src}/>
</div>

<style>
    .container {
        width: 100vw;
        height: 100vh;
        /* background-image: url(/img/test-0001.png); */
        /* background-repeat: no-repeat;
        background-size: contain;
        background-position: center; */
        background-color: black;
    }
</style>