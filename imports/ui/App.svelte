<script>
    import { Route } from 'tinro';
    import Home from "./Home.svelte";
    import ScreenSaver from "./ScreenSaver/ScreenSaver.svelte";
    import NotFound from "./NotFound.svelte";
</script>

<Route>
    <Route path="/"><Home /></Route>
    <Route path="/s"><ScreenSaver /></Route>
    <Route fallback><NotFound /></Route>
</Route>