<script>
    import App from "../App.svelte";
    import Home from "../Home.svelte";
    import ScreenSaver from "./ScreenSaver.svelte";
</script>

<!-- 来源：https://github.com/chokcoco/iCSS/issues/62 -->
<!-- 主要借助了滤镜 blur contrast 的融合效果-->
<!-- 尝试注释掉这一行 filter: blur(20px) contrast(30) -->
<!-- 完整详细内容：https://github.com/chokcoco/iCSS/issues/30-->

<div class="g-container">
    <div class="g-fire">
        {#each [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40] as a}
            <div class="g-dot" />
        {/each}
    </div>
</div>

<style>
    /* body {
        background: #000;
        overflow: hidden;
    } */
    :root {
        --fireWidth: 115px;
        --fireHeight: 200px;
        --dotSize: 24px;
        --fireColor: #b5932f;
    }
    .g-container {
        position: relative;
        width: var(--fireWidth);
        height: 300px;
        margin: 0;
        /* background-color: #000; */
    }
    .g-fire {
        position: absolute;
        width: 0;
        height: 0;
        bottom: 100px;
        left: 50%;
        border-radius: 45%;
        box-sizing: border-box;
        border: 200px solid #000;
        border-bottom: 200px solid transparent;
        transform: translate(-50%, 0) scaleX(0.4);
        background-color: var(--fireColor);
        filter: blur(20px) contrast(30);
    }
    .g-dot {
        position: absolute;
        bottom: -210px;
        left: 0;
        width: var(--dotSize);
        height: var(--dotSize);
        background: #000;
        border-radius: 50%;
    }
    .g-dot:nth-child(1) {
        bottom: -299px;
        left: 43px;
        animation: move 1.8s infinite 5.5s linear;
    }
    .g-dot:nth-child(2) {
        bottom: -331px;
        left: -153px;
        animation: move 0.8s infinite 1.9s linear;
    }
    .g-dot:nth-child(3) {
        bottom: -338px;
        left: -16px;
        animation: move 2.3s infinite 0.8s linear;
    }
    .g-dot:nth-child(4) {
        bottom: -272px;
        left: 52px;
        animation: move 1.6s infinite 5.1s linear;
    }
    .g-dot:nth-child(5) {
        bottom: -342px;
        left: -43px;
        animation: move 0.8s infinite 0.2s linear;
    }
    .g-dot:nth-child(6) {
        bottom: -360px;
        left: -146px;
        animation: move 1.1s infinite 4.2s linear;
    }
    .g-dot:nth-child(7) {
        bottom: -251px;
        left: 52px;
        animation: move 1.3s infinite 2.7s linear;
    }
    .g-dot:nth-child(8) {
        bottom: -350px;
        left: 131px;
        animation: move 3.3s infinite 0.9s linear;
    }
    .g-dot:nth-child(9) {
        bottom: -270px;
        left: 126px;
        animation: move 2.2s infinite 4.3s linear;
    }
    .g-dot:nth-child(10) {
        bottom: -323px;
        left: -152px;
        animation: move 1.1s infinite 5.9s linear;
    }
    .g-dot:nth-child(11) {
        bottom: -343px;
        left: 56px;
        animation: move 2.2s infinite 1.7s linear;
    }
    .g-dot:nth-child(12) {
        bottom: -251px;
        left: 102px;
        animation: move 3s infinite 3.6s linear;
    }
    .g-dot:nth-child(13) {
        bottom: -348px;
        left: -149px;
        animation: move 0.9s infinite 4.7s linear;
    }
    .g-dot:nth-child(14) {
        bottom: -276px;
        left: -134px;
        animation: move 0.9s infinite 2.8s linear;
    }
    .g-dot:nth-child(15) {
        bottom: -258px;
        left: 62px;
        animation: move 3.3s infinite 0.6s linear;
    }
    .g-dot:nth-child(16) {
        bottom: -309px;
        left: 5px;
        animation: move 2.6s infinite 4.7s linear;
    }
    .g-dot:nth-child(17) {
        bottom: -333px;
        left: -105px;
        animation: move 1.2s infinite 3.6s linear;
    }
    .g-dot:nth-child(18) {
        bottom: -349px;
        left: 26px;
        animation: move 1.6s infinite 1.8s linear;
    }
    .g-dot:nth-child(19) {
        bottom: -339px;
        left: 110px;
        animation: move 0.8s infinite 3.3s linear;
    }
    .g-dot:nth-child(20) {
        bottom: -284px;
        left: 42px;
        animation: move 1.6s infinite 0.8s linear;
    }
    .g-dot:nth-child(21) {
        bottom: -302px;
        left: -97px;
        animation: move 2s infinite 1.4s linear;
    }
    .g-dot:nth-child(22) {
        bottom: -257px;
        left: 21px;
        animation: move 1s infinite 5.6s linear;
    }
    .g-dot:nth-child(23) {
        bottom: -260px;
        left: 95px;
        animation: move 3.2s infinite 4.9s linear;
    }
    .g-dot:nth-child(24) {
        bottom: -343px;
        left: -96px;
        animation: move 1.7s infinite 5.5s linear;
    }
    .g-dot:nth-child(25) {
        bottom: -344px;
        left: -134px;
        animation: move 1.6s infinite 3.9s linear;
    }
    .g-dot:nth-child(26) {
        bottom: -252px;
        left: -130px;
        animation: move 2.4s infinite 3.4s linear;
    }
    .g-dot:nth-child(27) {
        bottom: -269px;
        left: -140px;
        animation: move 2.5s infinite 1.7s linear;
    }
    .g-dot:nth-child(28) {
        bottom: -255px;
        left: -48px;
        animation: move 2.3s infinite 2.7s linear;
    }
    .g-dot:nth-child(29) {
        bottom: -284px;
        left: 1px;
        animation: move 0.8s infinite 2.5s linear;
    }
    .g-dot:nth-child(30) {
        bottom: -295px;
        left: 92px;
        animation: move 1.2s infinite 0.7s linear;
    }
    .g-dot:nth-child(31) {
        bottom: -348px;
        left: 123px;
        animation: move 1.3s infinite 0.6s linear;
    }
    .g-dot:nth-child(32) {
        bottom: -315px;
        left: 51px;
        animation: move 2.5s infinite 3.9s linear;
    }
    .g-dot:nth-child(33) {
        bottom: -251px;
        left: -33px;
        animation: move 1.5s infinite 2.1s linear;
    }
    .g-dot:nth-child(34) {
        bottom: -313px;
        left: -153px;
        animation: move 2.1s infinite 2.9s linear;
    }
    .g-dot:nth-child(35) {
        bottom: -301px;
        left: -99px;
        animation: move 1.3s infinite 3.7s linear;
    }
    .g-dot:nth-child(36) {
        bottom: -286px;
        left: -11px;
        animation: move 1.1s infinite 3.6s linear;
    }
    .g-dot:nth-child(37) {
        bottom: -355px;
        left: 74px;
        animation: move 1.3s infinite 0.4s linear;
    }
    .g-dot:nth-child(38) {
        bottom: -251px;
        left: -155px;
        animation: move 0.8s infinite 4.5s linear;
    }
    .g-dot:nth-child(39) {
        bottom: -264px;
        left: 39px;
        animation: move 1.8s infinite 2.2s linear;
    }
    .g-dot:nth-child(40) {
        bottom: -308px;
        left: 88px;
        animation: move 1.6s infinite 2.6s linear;
    }
    @keyframes move {
        100% {
            transform: translate3d(0, -350px, 0);
        }
    }
</style>
