<script>
    import { page } from '$app/stores';
    export let href;
    export let title;
</script>

<li>
    <a {href} class:active="{$page.url.pathname == href}">{title}</a>
</li>

<style>

.active{
    text-decoration: underline;
}

</style>