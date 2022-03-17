<script>
    // import { onMount } from "svelte";
    import { Route } from 'tinro';
    import Home from "./Home.svelte";
    import ScreenSaver from "./ScreenSaver/ScreenSaver.svelte";
    import NotFound from "./NotFound.svelte";

</script>

<!-- <svelte:component this={route} /> -->

<!-- <Home/> -->
<!-- <ScreenSaver /> -->

<Route>
    <Route path="/"><Home /></Route>
    <Route path="/s"><ScreenSaver /></Route>
    <!-- <Route path="/f"><Fires /></Route> -->
    <Route fallback><NotFound /></Route>
</Route>