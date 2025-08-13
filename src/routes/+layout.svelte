<script lang="ts">
    import "../app.css";
    let { children } = $props();
    const favico: string =
        "https://raw.githubusercontent.com/hactuss/hactuss.github.io/refs/heads/main/img/favicon.jpg";
    const fav2: string = "https://hactuss.github.io/img/longcat.gif";
</script>

<svelte:head>
    <link rel="icon" href={fav2} />
    <title>Hactuss</title>
</svelte:head>

{@render children?.()}
