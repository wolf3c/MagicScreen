<script>
import { exclude_internal_props, query_selector_all } from "svelte/internal";

    import { router } from "tinro";
import App from "./App.svelte";

    const screens = [
        {
            id: "111",
            title: "鱼缸1",
            description: "这是一个鱼缸",
            img: "/img/test-0001.png",
        },
        {
            id: "222",
            title: "鱼缸2",
            description: "这是一个鱼缸",
            img: "/img/test-0001.png",
        },
        {
            id: "3",
            title: "鱼缸3",
            description: "这是一个鱼缸",
            img: "/img/test-0001.png",
        },
        {
            id: "4",
            title: "鱼缸4",
            description: "这是一个鱼缸",
            img: "/img/test-0001.png",
        },
    ];

    let isServiceOn = false;
    // $: isServiceOn  = false;
    let duration;

    function switchServiceState() {
        isServiceOn = !isServiceOn;
    }

    function changeDuration() {
        console.log(duration);
    }

    function scrollKeyEvent(e) {
        switch(e.keyCode) {
            case 37:
            case 21:
                // left key pressed
                this.previousElementSibling?.focus();
                break;
            case 38:
            case 19:
                // up key pressed
                this?.parentNode?.previousElementSibling?.firstChild?.focus()
                break;
            case 39:
            case 22:
                // right key pressed
                this.nextElementSibling?.focus();
                break;
            case 40:
            case 20:
                // down key pressed
                // document.querySelector("footer :first-child").focus();
                this?.parentNode?.nextElementSibling?.firstChild?.focus()
                break;  
            case 13:
            case 23:
                // enter key pressed
                // keyFuction?.enter();
                this.click();
                break;  
            case 27: // 27 为 ESC,  但是ESC首先要执行系统的事件，再执行html的事件。
            case 27: // 27 为 ESC,  但是ESC首先要执行系统的事件，再执行html的事件。
            case 4: // 4是遥控器的返回键
                // down key pressed
                break;  
            case 36:
                // Home key pressed
                break;  
        }   
        // on:keydown|preventDefault={(e) => scrollKeyEvent(e, this, {enter: function() {router.goto("/s")}})}
    }
</script>

<h1>Welcome to Magic Screen</h1>

<div class="horizontal-scroll" >
    {#each screens as s, i}
        <div
            class="scroll-item"
            tabindex="0"
            autofocus={i == 0 ? true : false}
            on:click={() => router.goto("/s")}
            on:keydown|preventDefault={scrollKeyEvent}
        >
            <img src={s.img} alt="" />
            <h5>{s.title}</h5>
            <p>{s.description}</p>
            <button>set</button>
        </div>
    {/each}
</div>
<footer>
    <button on:click={switchServiceState} on:keydown={scrollKeyEvent}
        >屏保功能已{#if isServiceOn}开启{:else}关闭{/if}</button
    >

    <select
        bind:value={duration}
        on:change={changeDuration}
        on:keydown={scrollKeyEvent}
        name="duration"
        id="duration_time"
    >
        <optgroup label="闲置多长时间进入屏保？" />
        <option value="3">3 分钟</option>
        <option value="5">5 分钟</option>
        <option value="10">10 分钟</option>
        <option value="15">15 分钟</option>
        <option value="20">20 分钟</option>
        <option value="30">30 分钟</option>
    </select>
    <span> 无操作，进入屏保 </span>
</footer>

<style>
    .horizontal-scroll {
        overflow-x: auto;
        scroll-snap-type: x mandatory;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }
    .horizontal-scroll::-webkit-scrollbar {
        display: none;
    }
    .scroll-item {
        scroll-snap-align: center;
        align-items: center;
        width: 90vw;
        margin: 0 1.25vw;
    }
    .scroll-item img {
        max-width: 90vw;
        max-height: 100%;
        display: block;
        margin: auto;
    }

    footer {
        position: fixed;
        bottom: 0;
        padding: 1rem 1rem 2rem 1rem;
    }
    footer > button {
        margin-right: 2rem;
    }
</style>
