<script>
    import {Link} from 'svelte-routing'; 

    

</script>






<div id="navbar">
    <div class="container">
        <div class="row row1">
            <ul class="largenav " style="padding-left: 70%;">
               <li class="upper-links"> <a class="links" href="/" >Login/SignUp</a></li>
                <li class="upper-links"> <a class="links" href="/"> <span class="far fa-bell"></span> </a> </li>
                <li class="upper-links dropdown"><a class="links" href="/">More</a>
                    <ul class="dropdown-menu">
                        <li class="profile-li"><a class="profile-links" href="/">Contact Us</a></li>
                        <li class="profile-li"><a class="profile-links" href="/">Advertise</a></li>
                    </ul>
                </li>
            </ul>
        </div>

        <div class="row row2">
            <div class="col-sm-2">
                <h1 style="margin:0px;"><span class="largenav">LOGO</span></h1>
            </div>
            <div class="navbar-search smallsearch col-sm-8 col-xs-11">
                <div class="row"> 
                    <input class="navbar-input col-xs-11" type="" placeholder="Search for Products, Brands and more" name="">
                </div>
            </div>
            <div class="cart largenav col-sm-2"> 
              <a class="cart-button" href="/"><span class="fas fa-shopping-cart"></span>
              </a> 
          </div>
        </div>

        <div class="row row3">
            <ul class="largenav pull-left" style="padding-left: 10%;">
                <Link to="/"> <li class="upper-links">Home</li></Link>
                <li class="upper-links dropdown">Shop <i class="fas fa-sort-down"></i>
                    <ul class="dropdown-menu">
                        <Link to="/laptop"><li class="profile-links">Laptop</li></Link>
                        <li class="profile-links">Computer</li>
                    </ul>
                </li>
            </ul>
        </div>

    </div>
</div>


<!-- Modal -->

