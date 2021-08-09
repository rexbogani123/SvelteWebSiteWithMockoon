<script>

import '../node_modules/bootstrap/dist/css/bootstrap.min.css';
import '../node_modules/jquery-confirm/dist/jquery-confirm.min.css';
import '../node_modules/jquery-confirm/dist/jquery-confirm.min.js';
import '../node_modules/@fortawesome/fontawesome-free/js/all';



import { Router, Route } from "svelte-routing";

import Navbar from '../src/Components/Navbar.svelte';
import Footer from '../src/Components/Footer.svelte';
import Home from '../src/Routes/Pages/Home.svelte';
import Shop from '../src/Routes/Pages/Shop.svelte';
import Payment from '../src/Routes/Pages/Payment.svelte';
import Laptop from '../src/Routes/Pages/Laptop.svelte';

</script>



<Router>
	<Navbar/>
		<Route path="/" component={Home}/>
		<Route path="/shope" component={Shop}/>			
		<Route path="/payment" component={Payment}/>
		<Route path="/laptop" component={Laptop}/>		
	<Footer/>
</Router>







