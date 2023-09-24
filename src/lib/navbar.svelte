<script>
  import Ham from "./ham.svelte";
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
</script>
<main>
<div class="navbar">
  <div class="logo"></div>
  <div class="ham" on:click={() => navOpen = !navOpen}><Ham/></div>
  <div class="links">
    <a class="link" href="#">Начало</a>

      <a class="link" on:mouseover={heh} on:mouseleave={() => isOpen = !isOpen} href="#">Кои сме ние?  <svg style="width: .7em; margin: 0"  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
        <path class="notactivesym" class:activesym = {isOpen} d="M4 17L25 39L46 17Z"  />
      </svg> 
      <div class:dropdown-content1={isOpen} class="dropdown-content2" style="position: absolute; display: flex;">
          <a href="#">Камара</a>
          <a href="#">Ръководство</a>
          <a href="#">Членове</a>
      </div>
    </a>
      <a class="link" on:mouseover={heh2} on:mouseleave={() => isOpen2 = !isOpen2} href="#">Документи <svg style="width: .7em; margin: 0"  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
        <path class="notactivesym" class:activesym = {isOpen2} d="M4 17L25 39L46 17Z"  />
      </svg> 
      <div class:dropdown-content1={isOpen2} class="dropdown-content2" style="position: absolute; display: flex;">
          <a href="#">Документи на ЕС</a>
          <a href="#">Документи на РБ</a>
          <a href="#">Документи на камарата</a>
      </div>
    </a>
      <a class="link" on:mouseover={heh3} on:mouseleave={() => isOpen3 = !isOpen3} href="#">Новини и събития <svg style="width: .7em; margin: 0"  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50">
        <path class="notactivesym" class:activesym = {isOpen3} d="M4 17L25 39L46 17Z"  />
      </svg> 
      <div class:dropdown-content1={isOpen3} class="dropdown-content2" style="position: absolute; display: flex;">
          <a href="#">Новини</a>
          <a href="#">Предстоящи събития</a>
          <a href="#">Информация за събития</a>
      </div>
    </a>
    <a class="link" href="#">Обяви</a>
    <a class="link" href="#">Полезни връзки</a>
    <a class="link" href="#">Контакти</a>
  </div>
</div>
<div class="sidebar" class:active = {navOpen}>
  <a href="#">Начало</a>
  <hr class="rounded">
  <a href="#">Камара</a>
  <hr class="rounded">
  <a href="#">Ръководство</a>
  <hr class="rounded">
  <a href="#">Членове</a>  <hr class="rounded">
  <a href="#">Документи на ЕС</a>  <hr class="rounded">
  <a href="#">Документи на РБ</a>  <hr class="rounded">
  <a href="#">Документи на камарата</a>  <hr class="rounded">
  <a href="#">Новини</a>  <hr class="rounded">
  <a href="#">Предстоящи събития</a>  <hr class="rounded">
  <a href="#">Информация за събития</a>  <hr class="rounded">
  <a  href="#">Обяви</a>  <hr class="rounded">
  <a  href="#">Полезни връзки</a>  <hr class="rounded">
  <a href="#">Контакти</a>  <hr class="rounded">

</div>
</main>
<style>

  .activesym{
fill: #1A936F !important;
transform: scale(100%) !important;
transition: all .1s;
}

  .notactivesym{
fill: #EDF7F6;
transform: scale(95%);
transition: all .1s;

}

    .navbar {
    background-color: #1e1b44;
    display: flex;
    /* position: fixed; */
    width:100%;
    /* padding: 0 3em; */
    min-height: 4em;
    height: 8vh;
    z-index: 10 !important; 
    justify-content: space-between;
    align-items: center;
}

.dropdown-content2{
  flex-direction: column;
  top: 1;
  z-index: 1;
  transform: translateY(-1em);
  background-color: #230846;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
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
    font-weight: 300 !important;
}

.navbar a:hover {
  color: #1A936F  
}

.sidebar {
  z-index: 1;
  width: 40vw;
  right: 0;
  top: 0;
  padding: 5% 0;
  border-radius: 1em 0 1em 1em;
  margin-top: 8vh;
  position: absolute;
  background-color: #5863F8;
  transition: all .5s;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  opacity: 0.75;
  clip-path: polygon(100% 0, 100% 0, 100% 100%, 100% 100%);

}
.sidebar a{
  color: #EDF7F6;
  text-decoration: none;
  width: 100%;
  font-size: 1.6rem;
  padding: 1em 0;
  font-weight: 350;
  text-align: center;


}
hr.rounded {
  border-radius: 12px;
  opacity: 0.15;
  width: 80%;
}
.sidebar a:hover{
  background-color: rgb(36, 29, 77);
}
.active {
  right: 0; /* Slide the sidebar into view when active */
  pointer-events: all;
  transition: all .5s;
  opacity: 1;
  clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
  

}

.navbar .logo {
    background-image: url("/logo_cee.png") ;
    margin-left: 2vw;
    width: 12em;
    height: 100%;
    background-position: center;
    background-size: cover;
}
.links{
  display: flex;
  height: 100%;
  margin-right: 2vw;
  align-items: center ;
  list-style-type: none;
  justify-content: space-between;
  gap: 2em;

}
.link{
  line-height: 8vh !important;

  
}

  /* Media query for responsive design */
  @media screen and (min-width: 1450px) {
    .ham{
      display: none;
      pointer-events: none;
      opacity: 0;
      z-index: -1;
    }
    
  }
  @media screen and (max-width: 1000px) {
    .sidebar {
  z-index: 1;
  width: 100%;
  right: 0;
  padding: 5% 0;
  border-radius: 0em 0em 1em 1em;
  margin-top: 8vh;
  position: absolute;
  background-color: #5863F8;
  transition: all .5s;
  display: flex;
  overflow-y: auto;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
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
  background-color: rgb(26, 21, 56);
}
.active {
  right: 0; /* Slide the sidebar into view when active */
  pointer-events: all;
  transition: all .5s;
  opacity: 1;
  clip-path: polygon(100% 0, 0 0, 0 100%, 100% 100%);

}
}

  @media screen and (max-width: 1450px) {

    /* Hide the links by default */
    .links {
      display: none;
      pointer-events: none;
      opacity: 0;
    }

  }

 
</style>