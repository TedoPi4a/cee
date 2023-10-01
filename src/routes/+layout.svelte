<script>
    import "$lib/main.css"
	import Nav2 from "$lib/nav2.svelte";
	import Navbar from "$lib/navbar.svelte";
	import Footer from "$lib/footer.svelte"
</script>

<Navbar/>
<slot/>
<div style="bottom: 0;">
<Footer/>
</div>
