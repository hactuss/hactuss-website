<main>
    <a href="/">BACK</a>
    <h1>♪ RandomSplatoonSongGiver (RELEASE Version 1.1) ♪</h1>
    <p id="info">
        <a href="javascript:toggle_message(info)"
            ><svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                ><path
                    fill="currentColor"
                    d="M5 3H3v18h18V3zm14 2v14H5V5zm-8 4H9V7H7v2h2v2h2v2H9v2H7v2h2v-2h2v-2h2v2h2v2h2v-2h-2v-2h-2v-2h2V9h2V7h-2v2h-2v2h-2z"
                /></svg
            ></a
        >
        Press 'Refresh' if the song does*nt play. There are only song snippets from
        inkipedia.org. and there's also a rare chance that it wont play any song,
        which I dont know how to fix. Feel free to message me on discord if you know
        something. I'd really apprechate :) Thank you for you visit!
    </p>
    <div class="contianer">
        <img src="" alt="AlbumCover" id="AlbumCover" draggable="false" />
        <h2 id="SongTitle">Songtitle</h2>
        <audio src="" id="Audio"><source src="" type="mpeg/mp3" /></audio>
        <!-- <div id="progressbar">
                <div id="Progress"><p></p></div>
            </div> -->
        <div id="buttons">
            <button id="PausePlay">Play/Pause</button>
            <button id="Refresh">Refresh</button>
        </div>
    </div>
</main>
<main>
    <p>Background Image, I am not the owner nor the creator of this image:</p>
    <p>Used in</p>
    <a href="https://splatoon.nintendo.com/base/en/gallery/"
        >https://splatoon.nintendo.com/base/en/gallery/</a
    >
    <p>file</p>
    <a
        href="https://splatoon.nintendo.com/base/_images/gallery/section-hero-splatoon-2-octo-medium-up.webp"
        >https://splatoon.nintendo.com/base/_images/gallery/section-hero-splatoon-2-octo-medium-up.webp</a
    >
    <p>Icons: <a href="https://pixelarticons.com/">pixelarticons.com</a></p>
</main>
<main><p>© Hactus 2025 - all rights reserved</p></main>

<style>
    html {
        background-image: url("https://splatoon.nintendo.com/base/_images/gallery/section-hero-splatoon-2-octo-medium-up.webp");
        background-size: cover;
    }
    nav {
        background-color: black;
        width: 100%;
        margin: 0;
        padding: 0;
        display: flex;
    }

    #AlbumCover {
        aspect-ratio: 1/1;
        width: 500px;
    }
    .contianer {
        padding-top: 10px;
        display: flex;
        flex-direction: column;
        align-items: center;
        background-color: rgba(0, 0, 0, 0.5);
        backdrop-filter: blur();
        margin-left: 12.5%;
        margin-right: 12.5%;
    }
    hr {
        width: 75%;
    }
    #PausePlay,
    #Refresh {
        width: 200px;
        height: 50px;
        margin: 20px;
        font-size: 25px;
        background-color: lime;
        border: none;
    }
    #PausePlay:active,
    #Refresh:active {
        width: 200px;
        height: 50px;
        margin: 20px;
        font-size: 25px;
        color: lime;
        background-color: rgba(0, 0, 0, 0.5);
        border: none;
    }

    #buttons {
        display: flex;
        justify-content: space-evenly;
    }

    @media only screen and (max-width: 500px) {
        #buttons {
            flex-direction: column;
        }
        nav {
            flex-direction: row;
            justify-content: center;
            width: 100%;
            height: 100%;
        }
        .nav-buttons:hover {
            background-color: rgb(131, 171, 255);
        }
    }
</style>
