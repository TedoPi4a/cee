<script>
  let isMenuOpen = false;

  function toggleMenu() {
    isMenuOpen = !isMenuOpen;
  }
</script>

<div class="navbar">
  <div class="logo"></div>
  <div class="hamburger-menu" class:active={isMenuOpen} on:click={toggleMenu}>
    <div></div>
    <div></div>
    <div></div>
  </div>
  <div class="links" class:open={isMenuOpen}>
    <a class="link" href="#">Начало</a>
    <div class="dropdown">
      <button class="dropbtn"><a href="#">Кои сме ние? ▾</a></button>
      <div class="dropdown-content">
        <a href="#">Камара</a>
        <a href="#">Ръководство</a>
        <a href="#">Членове</a>
      </div>
    </div>
    <div class="dropdown">
      <button class="dropbtn"><a href="#">Документи ▾</a></button>
      <div class="dropdown-content">
        <a href="#">Документи на ЕС</a>
        <a href="#">Ръководство</a>
        <a href="#">Членове</a>
      </div>
    </div>
    <a class="link" href="#">Контакти</a>
    <a class="link" href="#">Новини и събития</a>
    <a class="link" href="#">Обяви</a>
  </div>
</div>

<style>
    .navbar {
    background-color: #1e1b44;
    display: flex;
    padding: 0 1em;
    height: 10vh;
    z-index: 99999;
    justify-content: space-between;
    align-items: center;
}
        .dropdown {
  position: relative;
  display: inline-block;
          padding-left: 1em;
}
button{
  all: unset;

}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #230846;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
  margin: auto;
  padding: 0;
  width: 100%;
  min-width: fit-content;
  height: fit-content;
  border-radius:0 0 .4em .4em;
  font-weight: 300;

}

.dropdown-content a {
  color: black;
  font-size: 1.2em !important;

  padding: .8em 1em !important;
  text-decoration: none;
  display: block;
  font-family: 'Roboto', sans-serif;
  font-weight: 300;
}

.dropdown-content a:hover {background-color: #000000;
color: white !important;
}

.dropdown:hover .dropdown-content {
  display: block;
}

.dropdown:hover .dropbtn {
}
.dropbtn {
  cursor: pointer;
  color: #EDF7F6;
    text-decoration: none;
    padding-left: 1rem;
    font-size: 1.45rem;
    font-weight: 300;
    background-color: inherit;
    border: none;
    height: 100%;
}
.dropbtn :hover{
  color: #444444;
}
  .dropdown{
    height: 100%;
  }
.navbar a {
    color: #EDF7F6;
    text-decoration: none;
    font-size: 1.45rem;
    font-weight: 300 !important;
}

.navbar a:hover {
  color: #444444  
}


/* Optional: Style the logo */
.navbar .logo {
    background-image: url("/logo_cee.png") ;
    
    width: 12em;
    height: 100%;
    background-position: center;
    background-size: cover;
}
.links{
  display: flex;
  height: 100%;
  align-items: center ;
  list-style-type: none;
  justify-content: space-between;
  gap: 1rem;
}
.link{
  padding-left: 1em;
  
}
.hamburger-menu {
    display: none;
    flex-direction: column;
    cursor: pointer;
    transition: transform 0.3s ease; /* Added transition */
  }

  .hamburger-menu.active {
    transform: rotate(90deg); /* Rotate the icon when the menu is open */
  }

  .hamburger-menu div {
    width: 30px;
    height: 4px;
    background-color: white;
    margin: 4px 0;
    transition: background-color 0.3s ease; /* Added transition */
  }

  .hamburger-menu.active div {
    background-color: #1e1b44; /* Change color of icon bars when the menu is open */
  }

  /* Media query for responsive design */
  @media screen and (max-width: 768px) {
    /* Hide the logo on small screens */
    .navbar .logo {
      display: none;
    }

    /* Show the hamburger menu icon */
    .hamburger-menu {
      display: flex;
    }

    /* Hide the links by default */
    .links {
      display: none;
      flex-direction: column;
      position: absolute;
      top: 60px; /* Adjust as needed to avoid overlapping other content */
      right: 0;
      background-color: #1e1b44;
      width: 100%;
      transition: transform 0.3s ease, opacity 0.3s ease; /* Added transitions */
      transform: translateY(-100%); /* Hide the menu off-screen initially */
      opacity: 0;
    }

    .links.open {
      display: flex;
      transform: translateY(0); /* Slide in from the top */
      opacity: 1;
    }

    /* Style the dropdown content */
    .dropdown-content {
      background-color: #1e1b44;
      border: none;
      padding: 1rem;
      box-shadow: none;
    }

    .dropdown-content a {
      color: white;
      font-size: 1.2em;
      padding: 0.5rem 0;
      text-decoration: none;
      display: block;
      font-family: 'Roboto', sans-serif;
      font-weight: 300;
      transition: color 0.3s ease; /* Added transition */
    }

    .dropdown-content a:hover {
      color: #444444;
    }
  }

 
</style>