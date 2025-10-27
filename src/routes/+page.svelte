<script lang="ts">
    // import chartjs from "chartjs";
    import { onMount } from "svelte";
    import { derived } from "svelte/store";
    import { fade } from "svelte/transition";

    let top_bottom_text = "none";
    

    const options = {
        weekday: "short",
        hours: "2-digit",
        minutes: "2-digit",
        seconds: "2-digit",
    };
    
    const timezonede = "Europe/Berlin";
    
    let d = new Date();
    let dateoutde = d.toLocaleDateString(undefined, {timeZone: timezonede,});
    
    let timeoutde = $state("");
    
    function updatetime(){
        return (timeoutde = d.toLocaleTimeString(undefined, {
                timeZone: timezonede,
            }))
    }
    

    onMount(async () => {
        setInterval(() => {
            console.log(d.toLocaleTimeString(undefined, {
                timeZone: timezonede,
            }))
        }, 1);
    })
</script>

<main id="main-container">
    
        <div
            
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
                <a href="https://github.com/hactuss?tab=repositories">Github</a>
            </div>
        </div>
        <div id="window">
            <div id="bar"><p>time.hactuss.vercel.app</p></div>
            <div id="contents">
                <p>date: {dateoutde}</p>
                <p>time: {updatetime()}</p>
            </div>
        </div>
    </div>
</main>

<!-- rgb(82, 104, 219) -->

<style>
    * {
        cursor: url('https://psychoslinux.gitlab.io/images/Cursor_RetroWave_Normal.gif'), auto;
    }
    *::selection{
        background-color: rgb(55 253 77);
        color: rgb(200 250 20);
    }

    a {
        display: block;
    }
    h1 {
        text-wrap-mode: nowrap;
    }
    main {
        display: flex;
    }

    #window {
        border: solid 2px black;
        margin: 10px;
        background-color: rgb(20, 20, 20);
    }
    #bar {
        background-color: rgb(200 250 20);
        color: black;
        border-bottom: solid black 2px;
        font-size: 0.75rem;
        padding: 2px;
    }
    #option-bar {
        padding: 0px;
        background-color: rgb(230, 230, 230);
        width: 100%;
        height: 100%;
    }
    button,
    #button {
        border-radius: 0px;
        background-color: rgb(220, 220, 220);
    }
    #contents {
        margin: 10px;
        display: flex;
        flex-direction: column;
        background-color: rgb(20, 20, 20);
    }
    #dropdown {
        background-color: rgb(230, 230, 230);
        width: auto;
        max-width: 450px;
        border: solid black 1px;
        text-wrap: inherit;
        margin: 4px;
        position: absolute;
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 5px;
    }
    #img {
        width: 150px;
        margin: 25px;
    }
    a {
        display: inline-block;
    }
</style>
