<script>
    import "$lib/main.css"
	import Navbar from "$lib/navbar.svelte";
    let isVisible = false

</script>
<!-- <div class="navbar">
    <div class="dropdown" on:mouseenter={() => isVisible = !isVisible}>
        <p>Hey, click here</p>
       {#if isVisible}
       <div class="dropdown-content">
        <a href="">Hey</a>
    </div>
       {/if}

    </div>
</div> -->
<Navbar/>
<slot/>


<style>
    .dropdown{
    }
    .dropdown-content{
        position: absolute;
        height: 20em;
        width: 10%;
        background-color: rgb(61, 61, 61);
    }
    .dropdown-content a{
        color: white;
        text-decoration: none;
    }
    .navbar{
        background-color: bisque;
        margin: 0;
        padding: 0;
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .navbar p{
    }
</style>