<script>

</script>
<main>
    <header>
        <nav>
            <ul class="nav-area">
               <li><a href="/"><b>Ltop</b></a></li>
               <li><a href="/"><b>Home</b></a></li>
               <li><a href="/ltop/aboutus"><b>About Us</b></a></li>
               <li><a href="/ltop/contactus"><b>Contact Us</b></a></li>
            </ul>
        </nav>
        <ul>
            <div class="dropdown">
                <button class="dropbtn">Dropdown</button>
                <div class="dropdown-content">
                <a href="/Tech/techlog">Become a technician</a>
                <a href="/Worker/worklog">Become a worker</a>
                </div>
             </div>
        <a href="/ltop/login" class="btn-area">Login</a>
        <a href="/ltop/signup" id="res" class="btn-area">Sign-up</a>
        <a href="/ltop/logout" class="btn-area">Logout</a>
    </ul>
    </header>
</main>

<style>
main{
    background-color: black;
}
a{
     text-decoration: none;
}
header{
    display: -webkit-flex;
    display: -moz-flex;
    display: -ms-flex;
    display: -o-flex;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px;
}
.nav-area{
    list-style:none;
}
.nav-area li{
    display: inline-block;
    padding: 0 15px;
    text-transform: uppercase;
}
.nav-area li a{
    color: #fff;
}
.nav-area li a:hover{
    color: #006c87;
}
.btn-area{
    cursor: pointer;
    color: #fff;
    font-size: 16px;
    letter-spacing: 2px;
    text-transform: uppercase;
    padding: 10px 30px;
    border-radius: 5px;
    background: #006c87;
}
#res{
    cursor: pointer;
    color: #fff;
    font-size: 16px;
    letter-spacing: 2px;
    text-transform: uppercase;
    padding: 10px 30px;
    border-radius: 5px;
    background:green; 
}
.dropbtn {
  background-color: #4CAF50;
  color: white;
  padding: 16px;
  font-size: 16px;
  border: none;
  cursor: pointer;
}

.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

.dropdown-content a:hover {background-color: #f1f1f1}

.dropdown:hover .dropdown-content {
  display: block;
}

.dropdown:hover .dropbtn {
  background-color: #3e8e41;
}
</style>