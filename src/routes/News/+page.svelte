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
    <title>News</title> 
</svelte:head>
{news.title}
<div id="news-img"><img src="{news.img}"></div>
{news.article}