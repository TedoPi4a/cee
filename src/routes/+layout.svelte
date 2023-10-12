<script>
    import "$lib/main.css"
	import { page } from '$app/stores';
	import Nav2 from "$lib/nav2.svelte";
	import Navbar from "$lib/navbar.svelte";
	import Footer from "$lib/footer.svelte";
	
</script>

<Navbar/>
{#if $page.url.pathname === "/"}
	<slot/>
	{:else}
	<main>
	<h1 style="font-size: clamp(2.6rem, 8vw, 4rem); margin-bottom: 25vh; text-align: center">Очаквайте скоро!</h1>
</main>
{/if}
<div style="bottom: 0;">
<Footer/>
</div>

<style>
	main{
		width: 100%;
		max-width: 100%;
		margin: 0 auto;
		height: calc(100vh - 5em);
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
