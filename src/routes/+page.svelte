<main id="main-container" class="flex justify-center content-center">
    <div class="bg-black w-[100%] h-[100%] flex-1/8">
        <h1
            style="font-size: 9rem; writing-mode: vertical-lr; align-bottom"
            class="text-white text-center"
        >
            Hactus
        </h1>
    </div>
    <div class="w-[100%]">
        <div
            class="flex flex-col justify-center items-center"
            style="justify-self: center;"
        ></div>
        <div id="window" class="m-[10px]">
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
    </div>
</main>

<!-- rgb(82, 104, 219) -->

<style>
    a {
        display: block;
    }

    #window {
        border: solid 2px black;
    }
    #bar {
        background-color: black;
        color: white;
        font-size: 0.75rem;
        padding: 2px;
    }
    #contents {
        margin: 10px;
    }
</style>
