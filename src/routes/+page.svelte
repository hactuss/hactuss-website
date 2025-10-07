<script lang="ts">
    import { onMount } from "svelte";
    import { derived } from "svelte/store";

    let top_bottom_text = "none";
    let side_text = "block";

    const options = {
        weekday: "short",
        hours: "2-digit",
        minutes: "2-digit",
        seconds: "2-digit",
    };
    let timeoutde = $state("");
    let dateoutde = "";
    const timezonede = "Europe/Berlin";
    let d = $state(new Date());

    let countdown = $derived(d.getSeconds());

    dateoutde = timeoutde = d.toLocaleDateString(undefined, {
        timeZone: timezonede,
    });
    onMount(() => {
        setInterval(() => {
            return (timeoutde = d.toLocaleTimeString(undefined, {
                timeZone: timezonede,
            }));
        }, 1000);
    });
</script>

<main id="main-container" class="flex justify-center content-center">
    <div
        style="display: {side_text};"
        class="bg-black w-[100%] h-[100%] flex-1/8"
    >
        <h1
            style="font-size: 9rem; writing-mode: vertical-lr; align-bottom"
            class="text-white text-center"
        >
            H a c t u s
        </h1>
    </div>

    <div class="w-[100%]">
        <div
            id="top_bottom_text"
            style="display: {top_bottom_text}; color: white; background-color: black;"
        >
            <div><h1>HACTUS</h1></div>
        </div>
        <div
            class="flex flex-col justify-center items-center"
            style="justify-self: center;"
        ></div>
        <div id="window">
            <div id="bar"><p>+hactuss.svelte</p></div>
            <div id="contents">
                <a href="https://office-haj.vercel.app">go to the office</a>
                <a href="https://isitspookymonth.vercel.app"
                    >is it spooky month?</a
                >
                <a href="/radio">radio</a>
                <a href="/videos">videos</a>
                <a href="/randomplay">randomplayer</a>
                <a
                    href="https://github.com/hactuss?tab=repositories"
                    target="_blank">Github</a
                >
            </div>
        </div>
        <!--
        <div id="window">
            <div id="bar"><p>timezone.svelte</p></div>
            <div id="contents">
                <h2>
                    {timeoutde}
                </h2>
                <h2>
                    {dateoutde}
                </h2>
                <h2>
                    {() => {}}
                </h2>
            </div>
            <div
                id="top_bottom_text"
                style="display: {top_bottom_text}; color: white; background-color: black; position: relative; bottom: 0;"
            >
                <div><h1>HACTUS</h1></div>
            </div>
        </div> -->
    </div>
</main>

<!-- rgb(82, 104, 219) -->

<style>
    a {
        display: block;
    }
    h1 {
        text-wrap-mode: nowrap;
    }

    #window {
        border: solid 2px black;
        margin: 10px;
    }
    #bar {
        background-color: rgb(200 250 20);
        color: black;
        font-size: 0.75rem;
        padding: 2px;
    }
    #contents {
        margin: 10px;
    }
</style>
