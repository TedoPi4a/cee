<div class="navbar">
    <img class="logo" src="/logo_cee.png" alt="">
   <div class="links"> <a href="#">Начало</a>
    <a href="#">Контакти</a>
       
    <div class="dropdown">
        <a class="dropbtn">Кои сме ние?        <div class="dropdown-content">
            <a href="#">Камара</a>
            <a href="#">Ръководство</a>
            <a href="#">Членове</a>
        </div></a>

  </div>
    <div class="dropdown">
        <a class="dropbtn">Документи
            <div class="dropdown-content">
                <a href="#">Документи на ЕС</a>
                <a href="#">Документи на РБ</a>
                <a href="#">Членове</a>
            </div>
        </a>
 
  </div>
 
    <a href="#">Новини и събития</a>
    <a href="#">Обяви</a>
</div>
</div>

<style>
            .navbar {
            background-color: #1e1b44;
            display: flex;
            padding: 0 2em;
            justify-content: space-between;
            align-items: center;
        }

        .navbar a {
            color: #EDF7F6;
            text-decoration: none;
            padding: 0 1.1em;
            font-size: 1.45rem;
            font-weight: 360;
        }

        .navbar a:hover {
            color: #1A936F;
        }

        /* Optional: Style the logo */
        .navbar .logo {
            
            width: 14rem;
        }
        .dropbtn {
  position: relative;
  cursor: pointer;
  z-index: 1111;
}


.dropdown {
  display: inline-block;
  width: fit-content;
  position: relative;
  z-index: 11111;
}

.dropdown-content {
  display: none;
  bottom: -1;
  border-radius: 0 0 .4em .4em;
  position: absolute;
  width: 100%;
  background-color: #1A936F;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1111;
}

.dropdown-content a {
  padding: .8em;
  text-decoration: none;
  display: block;
}

.dropdown-content a:hover {background-color: #edf7f6}

.dropdown:hover .dropdown-content {
  display: block;
}


</style>