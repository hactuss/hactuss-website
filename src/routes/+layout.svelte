<script lang="ts">
    import "../app.css";
    let { children } = $props();
    const favico: string =
        "https://raw.githubusercontent.com/hactuss/hactuss.github.io/refs/heads/main/img/favicon.jpg";
    const fav2: string = "https://hactuss.github.io/img/longcat.gif";
    const fav3: string =
        "https://i.kym-cdn.com/photos/images/original/000/090/166/Awesome-120110725-22047-1faqsqh.gif";
</script>

<svelte:head>
    <link rel="icon" href={fav3} />
    <title>Hactuss</title>
</svelte:head>

{@render children?.()}
