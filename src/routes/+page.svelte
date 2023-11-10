<script>
    import {onMount} from "svelte";
    let news = [];
    onMount(async () => {
        let res = await fetch ('https://gist.githubusercontent.com/Daniel2003Morris/d8fc523007d436e4915232704038d307/raw/5d54145c2ca5a50250fddcd659c393cd59731ff6/galnet.json')
        news = await res.json();
        console.log(news)
    })
</script>
<svelte:head>
    <title>Index</title> 
</svelte:head>
<video autoplay muted loop id="indexVideo">
    <source src="indexVideo.mp4" type="video/mp4" alt="Unable to play media">
</video>
<div id="index-border"></div>
<div id="grid-container">
    <div id="news-img"><img src="{news.img}"></div>
    <div id="news-txt">
        {news.article}
    </div>
    <div id="news-txt">
        placeholder
    </div>
    <div id="news-img"></div>
    <div id="news-img"></div>
    <div id="news-txt">
        placeholder
    </div>
</div>