<script>
  import Ham from "./ham.svelte";
  import { page } from '$app/stores';
	import { fly, fade } from "svelte/transition";

let isOpen = false;
let isOpen2 = false;
let isOpen3 = false;

let navOpen = false
  function heh() {
    isOpen = true;
  }
  function heh2() {
    isOpen2 = true;
  }
  function heh3() {
    isOpen3 = true;
  }
  function idk(){
    navOpen = false;
    isOpen = false;
    isOpen2 = false;
    isOpen3 = false
  }
</script>
<main>
<div on:mouseleave={idk} class="navbar">

 <a class="logo" href="/"></a>
  <div class="ham" on:click={() => navOpen = !navOpen}><Ham isHam={navOpen} /></div>
  <div class="links">
    <a class:is-active2={$page.url.pathname === "/"} class="link" href="/">Начало</a>

      <a class="link" on:mouseover={heh} on:mouseleave={() => isOpen = !isOpen} href="/info">Кои сме ние?  <svg style="width: .7em; margin: 0"  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
        <path class="notactivesym" class:activesym = {isOpen} d="M4 17L25 39L46 17Z"  />
      </svg> 
      <div class:dropdown-content1={isOpen} class="dropdown-content2" style="position: absolute; display: flex;"> 
          <a class:is-active2={$page.url.pathname === "/chamber"} href="/chamber">Камара</a>
          <a class:is-active2={$page.url.pathname === "/managment"} href="/managment">Ръководство</a>
          <a class:is-active2={$page.url.pathname === "/members"} href="/members">Членове</a>
      </div>
    </a>
      <a class="link" on:mouseover={heh2} on:mouseleave={() => isOpen2 = !isOpen2} href="#">Документи <svg style="width: .7em; margin: 0"  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
        <path class="notactivesym" class:activesym = {isOpen2} d="M4 17L25 39L46 17Z"  />
      </svg> 
      <div class:dropdown-content1={isOpen2} class="dropdown-content2" style="position: absolute; display: flex;">
          <a class:is-active2={$page.url.pathname === "/eu-documents"} href="/eu-documents">Документи на ЕС</a>
          <a class:is-active2={$page.url.pathname === "/bulgarian-documents"} href="/bulgarian-documents">Документи на РБ</a>
          <a class:is-active2={$page.url.pathname === "/cee-documents"} href="/cee-documents">Документи на камарата</a>
      </div>
    </a>
      <a class="link" on:mouseover={heh3} on:mouseleave={() => isOpen3 = !isOpen3} href="#">Новини и събития <svg style="width: .7em; margin: 0"  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
        <path class="notactivesym" class:activesym = {isOpen3} d="M4 17L25 39L46 17Z"  />
      </svg> 
      <div class:dropdown-content1={isOpen3} class="dropdown-content2" style="position: absolute; display: flex;">
          <a class:is-active2={$page.url.pathname === "/news"} href="/news">Новини</a>
          <a class:is-active2={$page.url.pathname === "/upcoming-events"} href="/upcoming-events">Предстоящи събития</a>
          <a class:is-active2={$page.url.pathname === "/events-information"} href="/events-information">Информация за събития</a>
      </div>
    </a>
    <a class="link" class:is-active2={$page.url.pathname === "/trainings"}   href="/trainings">Обучения</a>
    <a class="link" class:is-active2={$page.url.pathname === "/useful-links"} href="/useful-links">Полезни връзки</a>
    <a class="link" class:is-active2={$page.url.pathname === "/contacts"} href="/contacts">Контакти</a>
  </div>
  <div class="sidebar"  class:active = {navOpen} >
    <div class="sidebar-links">
    <a on:click={idk} class:is-active3={$page.url.pathname === "/"} href="/">Начало</a>
    <hr class="rounded">
    <a on:click={() => isOpen = !isOpen} class:is-active={isOpen} href="#">Кои сме ние? <svg style="width: .7em; margin: 0"  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
      <path class="notactivesym" class:activesym = {isOpen} d="M4 17L25 39L46 17Z"  />
    </svg> </a>
    {#if isOpen}
    <a in:fly={{ x: 100, duration: 200 }} out:fade={{duration: 200}} on:click={idk} href="/info">Информация </a>
    <a in:fly={{ x: 100, duration: 200 }} out:fade={{duration: 200}} on:click={idk} class:is-active3={$page.url.pathname === "/chamber"} href="/chamber">Камара</a>
    <a in:fly={{ x: 100, duration: 200 }} out:fade={{duration: 200}} on:click={idk} class:is-active3={$page.url.pathname === "/managment"} href="/managment">Ръководство</a>
    <a in:fly={{ x: 100, duration: 200 }} out:fade={{duration: 200}} on:click={idk} class:is-active3={$page.url.pathname === "/members"} href="/members">Членове</a>  <hr class="rounded">
    {:else}
    <hr class="rounded">
    {/if}
   
    <a on:click={() => isOpen2 = !isOpen2} class:is-active={isOpen2} href="#">Документи <svg style="width: .7em; margin: 0"  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
      <path class="notactivesym" class:activesym = {isOpen2} d="M4 17L25 39L46 17Z"  />
    </svg> </a>
    {#if isOpen2}
    <a in:fly={{ x: 100, duration: 200 }} out:fade={{duration: 200}} on:click={idk} style="line-height: 1.4em" class:is-active3={$page.url.pathname === "/eu-documents"} href="/eu-documents">Документи на ЕС</a>  
    <a in:fly={{ x: 100, duration: 200 }} out:fade={{duration: 200}} on:click={idk} style="line-height: 1.4em" class:is-active3={$page.url.pathname === "/bulgarian-documents"} href="/bulgarian-documents">Документи на РБ</a>  
    <a in:fly={{ x: 100, duration: 200 }} out:fade={{duration: 200}} on:click={idk} style="line-height: 1.4em" class:is-active3={$page.url.pathname === "/cee-documents"} href="/cee-documents">Документи на камарата</a>  <hr class="rounded">
    {:else}
    <hr class="rounded">
    {/if}
    <a on:click={() => isOpen3 = !isOpen3} class:is-active={isOpen3} href="#">Новини и събития <svg style="width: .7em; margin: 0"  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
      <path class="notactivesym" class:activesym = {isOpen3} d="M4 17L25 39L46 17Z"  />
    </svg> </a>
    {#if isOpen3}
    <a in:fly={{ x: 100, duration: 200 }} out:fade={{duration: 200}} on:click={idk} class:is-active3={$page.url.pathname === "/news"} href="/news">Новини</a>  
    <a in:fly={{ x: 100, duration: 200 }} out:fade={{duration: 200}} on:click={idk} class:is-active3={$page.url.pathname === "/upcoming-events"} href="/upcoming-events">Предстоящи събития</a> 
    <a in:fly={{ x: 100, duration: 200 }} out:fade={{duration: 200}} on:click={idk} class:is-active3={$page.url.pathname === "/events-information"} href="/events-information">Информация за събития</a>  <hr class="rounded">
    {:else}
    <hr class="rounded">
    {/if}



    <a on:click={idk} class:is-active3={$page.url.pathname === "/trainings"} href="/trainings">Обучения</a>  <hr class="rounded">
    <a on:click={idk} class:is-active3={$page.url.pathname === "/useful-links"} href="/useful-links">Полезни връзки</a>  <hr class="rounded">
    <a on:click={idk} class:is-active3={$page.url.pathname === "/contacts"} href="/contacts">Контакти</a>  <hr class="rounded">
  </div>
</div>

</div>
</main>
<style>
.dropdown-sidebar{
  opacity: 0;
  pointer-events: none;
  transition: all .5s;
  position: relative;
  width: 100%;
}
.dropdown-sidebar .active{
  opacity: 1;
  
}
  .activesym{
fill: #3d8989 !important;
transform: scale(100%) !important;
transition: all .1s;
}

  .notactivesym{
fill: #EDF7F6;
transform: scale(95%);
transition: all .1s;

}

.is-active2{
  font-weight: 400 !important;
  color: var(--blue) !important;  
}
.is-active{
  /* background-color: #3f48b3c4 !important; */
  background-color: #136b51 !important;

}

.is-active3{
  font-weight: 400 !important;
  background-color: #0d4937!important;  
 

}

    .navbar {
    background-color: var(--nav);
    display: flex;
    position: relative;
    /* position: fixed; */
    width:100%;
    /* padding: 0 3em; */
    height: 5em;
    z-index: 10 !important; 
    justify-content: space-between;
    align-items: center;
}

.dropdown-content2{
  flex-direction: column;
  top: 1;
  z-index: 1;
  transform: translateY(-1em);
  background-color: var(--nav);
  /* box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2); */
  line-height: 3em;
  min-width: fit-content;
  height: fit-content;
  border-radius:0 0 .5em .5em;
  font-weight: 300;
  display: none;
  pointer-events: none;
  opacity: 0;
  margin-left: -.3em;
  display: none;
transition: all .2s;}
.dropdown-content1{
  opacity: 1;
  transition: all .2s;
pointer-events: all;
transform: none;
display: block;
}



.dropdown-content2 :last-child{
  border-radius:0 0 .5em .5em;

}
.dropdown-content2 a {
  color: black;

  font-size: .8em !important;
  padding: 0 1em;
  text-decoration: none;
  display: block;
  font-weight: 300;
}

.dropdown-content2 a:hover {
  background-color: #1A936F;
color: white !important;
}


.navbar a {
    color: #EDF7F6;
    text-decoration: none;
    font-size: 1.45rem;
    font-weight: 300;
    text-transform: uppercase;
}

.navbar a:hover {
  color: var(--blue)  
}

.sidebar {
  z-index: 1;
  width: 30vw;
  right: 0;
  top: 0;
  height: calc(100vh - 5rem);
  margin-top: 5rem;
  overflow-y: auto;
  border-radius: 0 0 1em 1em;
  position: absolute;
  background-color: var(--nav);
  transition: all .5s;
  overflow-x: hidden;
  opacity: 0.75;
  clip-path: polygon(100% 0, 100% 0, 100% 100%, 100% 100%);

}
.sidebar::-webkit-scrollbar-thumb {
    background-color: #424242 !important;}

  .sidebar::-webkit-scrollbar {
    width: .5rem;
    
  }  
.sidebar-links{
  display: flex;
  flex-direction: column;
  padding-top: 1em;
  justify-content: flex-start;
  align-items: center;
}

.sidebar a{
  color: #EDF7F6;
  text-decoration: none;
  width: 100%;
  font-size: 1.6rem;
  padding: .6em 0;
  font-weight: 350;
  text-align: center;


}
hr.rounded {
  border-radius: 12px;
  opacity: 0.15;
  width: 80%;
  margin: .2rem;
}
.sidebar a:hover{
  /* background-color: rgb(49, 40, 100) !important; */
  background-color: #178b69;
  color: #EDF7F6 !important;
}
.active {
  right: 0; /* Slide the sidebar into view when active */
  pointer-events: all;
  transition: all .5s;
  opacity: 1;
  clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
  

}

 .logo {
    background-image: url("/cee_logo_.png") ;
    margin-left: 2vw;
    width: 6em;
    height: 100%;
    background-position: center;
    background-size: contain;
    background-repeat: no-repeat;
}
.links{
  display: flex;
  height: 100%;
  margin-right: 2vw;
  align-items: center ;
  list-style-type: none;
  justify-content: space-between;
  gap: 2.4em;

}
.link{
  line-height: 5rem !important;

  
}

  /* Media query for responsive design */
  @media screen and (min-width: 1600px) {
    .ham{
      display: none;
      pointer-events: none;
      opacity: 0;
      z-index: -1;
    }
    
  }
  @media screen and (max-width: 1599px) {

/* Hide the links by default */
.links {
  display: none;
  pointer-events: none;
  opacity: 0;
}

}
  @media screen and (max-width: 1000px) {
    .sidebar::-webkit-scrollbar {
    visibility: hidden;
    opacity: 0;
    display: none;
    
  }  
    .sidebar {
  width: 100vw;
  margin-left: auto;
  margin-right: auto;
      height: calc(100svh - 5rem) ;
  /* background-color: #5863F8; */
  background-color: var(--nav);
  border-radius: 0 0 1em 1em;

  opacity: 0.85;
  clip-path: polygon(100% 0, 0 0, 0 0, 100% 0);
}
.sidebar a{
  color: #EDF7F6;
  text-decoration: none;
  width: 100%;
  font-size: 1.4em;
  padding: 1em 0;
  text-align: center;
}
.sidebar a:hover{
  /* background-color: rgb(26, 21, 56); */
}
.active {
  right: 0; /* Slide the sidebar into view when active */
  pointer-events: all;
  transition: all .5s;
  opacity: 1;
  clip-path: polygon(100% 0, 0 0, 0 100%, 100% 100%);

}
}



 
</style>