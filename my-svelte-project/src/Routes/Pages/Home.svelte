<script>
import {Link} from 'svelte-routing'; 

import Modal from './Modal.svelte';

let showModal = false;
</script>

<style>
 @import url(https://fonts.googleapis.com/css?family=Calibri:400,300,700);

.mt-100 {
    margin-top: 10px
}

.product-wrapper,
.product-img {
    overflow: hidden;
    position: relative
}

.mb-45 {
    margin-bottom: 10px
}

.product-action {
    bottom: 0px;
    left: 0;
    opacity: 0;
    position: absolute;
    right: 0;
    text-align: center;
    transition: all 0.6s ease 0s
}

.product-wrapper {
    border-radius: 10px
}

.product-img>span {
    background-color: #fff;
    box-shadow: 0 0 8px 1.7px rgba(0, 0, 0, 0.06);
    color: #333;
    display: inline-block;
    font-size: 12px;
    font-weight: 500;
    left: 20px;
    letter-spacing: 1px;
    padding: 3px 12px;
    position: absolute;
    text-align: center;
    text-transform: uppercase;
    top: 20px
}

.product-action-style {
    background-color: #fff;
    box-shadow: 0 0 8px 1.7px rgba(0, 0, 0, 0.06);
    display: inline-block;
    padding: 16px 2px 12px
}

.product-action-style>a {
    color: #979797;
    line-height: 1;
    padding: 0 21px;
    position: relative
}

.product-action-style>a.action-plus {
    font-size: 18px
}

.product-wrapper:hover .product-action {
    bottom: 20px;
    opacity: 1
}




.container {
    margin: 30px auto
}

.container .product-item .product img {
    width: 100%;
    height: 100%;
    object-fit: cover
}



@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800&display=swap");

.card {
    border: none;
    border-radius: 10px
}

.percent {
    padding: 5px;
    background-color: red;
    border-radius: 5px;
    color: #fff;
    font-size: 14px;
    height: 35px;
    width: 70px;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer
}

.wishlist {
    height: 40px;
    width: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
    background-color: #eee;
    padding: 10px;
    cursor: pointer
}

.img-container {
    position: relative
}

.img-container .first {
    position: absolute;
    width: 100%
}

.img-container img {
    border-top-left-radius: 5px;
    border-top-right-radius: 5px
}

.product-detail-container {
    padding: 10px
}

.ratings i {
    color: #a9a6a6
}

.ratings span {
    color: #ffffff
}
.card-header {
    background-color: rgb(255, 255, 255);
    color: rgb(38, 34, 75);
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
}
.card-body{

   background-color: rgb(255, 145, 19);
}
</style>


 <!--Top -->
<div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="Image/83.jpg" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img src="Image/83.jpg" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img src="Image/83.jpg" class="d-block w-100" alt="...">
      </div>
    </div>
    <button   class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button  on:click="{() => showModal = true}" class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>

 <!--Middle -->
 
 <div class="card">
   <h5 class="card-header text-center">Featured</h5>
   <div class="card-body">
     <div class="row">
      <div class="container d-flex justify-content-center mt-100">
        <div class="row">
            <div class="col-md-3">
                <div class="product-wrapper mb-45 text-center">
                    <div class="product-img"> <a href="/" data-abc="true"> <img src="https://i.imgur.com/tL7ZE46.jpg" alt=""> </a> <span class="text-center"><i class="fas fa-dollar-sign"></i> 43,000</span>
                        <div class="product-action">
                            <div class="product-action-style">
                                 <a href="/"><i class="fa fa-plus"></i> </a>
                                  <a href="/" > <i class="fa fa-heart"></i> </a> 
                                  <button on:click="{() => showModal = true}"> <i class="fa fa-shopping-cart"></i> </button> 
                                </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="product-wrapper mb-45 text-center">
                    <div class="product-img"> <a href="/" data-abc="true"> <img src="https://i.imgur.com/lAQxXCK.jpg" alt=""> </a> <span><i class="fas fa-dollar-sign"></i> 41,000</span>
                        <div class="product-action">
                            <div class="product-action-style"> <a class="action-plus" title="Quick View" data-toggle="modal" data-target="#exampleModal" href="/" data-abc="true"> <i class="fa fa-plus"></i> </a> <a class="action-heart" title="Wishlist" href="/" data-abc="true"> <i class="fa fa-heart"></i> </a> <a class="action-cart" title="Add To Cart" href="/" data-abc="true"> <i class="fa fa-shopping-cart"></i> </a> </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
              <div class="product-wrapper mb-45 text-center">
                  <div class="product-img"> <a href="/" data-abc="true"> <img src="https://i.imgur.com/lAQxXCK.jpg" alt=""> </a> <span><i class="fas fa-dollar-sign"></i> 41,000</span>
                      <div class="product-action">
                          <div class="product-action-style"> <a class="action-plus" title="Quick View" data-toggle="modal" data-target="#exampleModal" href="/" data-abc="true"> <i class="fa fa-plus"></i> </a> <a class="action-heart" title="Wishlist" href="/" data-abc="true"> <i class="fa fa-heart"></i> </a> <a class="action-cart" title="Add To Cart" href="/" data-abc="true"> <i class="fa fa-shopping-cart"></i> </a> </div>
                      </div>
                  </div>
              </div>
          </div>
            <div class="col-md-3">
                <div class="product-wrapper mb-45 text-center">
                    <div class="product-img"> <a href="/" data-abc="true"> <img src="https://i.imgur.com/lAQxXCK.jpg" alt=""> </a> <span><i class="fas fa-dollar-sign"></i> 23,000</span>
                        <div class="product-action">
                            <div class="product-action-style"> <a class="action-plus" title="Quick View" data-toggle="modal" data-target="#exampleModal" href="/" data-abc="true"> <i class="fa fa-plus"></i> </a> <a class="action-heart" title="Wishlist" href="/" data-abc="true"> <i class="fa fa-heart"></i> </a> <a class="action-cart" title="Add To Cart" href="/" data-abc="true"> <i class="fa fa-shopping-cart"></i> </a> </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
     </div>
   </div>
 </div>

<!--Buttom -->

 <div class="card">
   <h5 class="card-header text-center">SALE</h5>
   <div class="card-body">
     <div class="row">
      <div class="col-md-4">
        <div class="card">
            <div class="img-container">
                <div class="d-flex justify-content-between align-items-center p-2 first">
                   <span class="percent">-25%</span> <span class="wishlist">
                     <i class="fa fa-heart"></i>
                    </span> 
                </div>
                 <img alt="" src="Image/83.jpg" class="img-fluid">
            </div>
            <div class="product-detail-container">
                <div class="d-flex justify-content-between align-items-center">
                    <h6 class="mb-0">Dell Laptop</h6> <span class="text-danger font-weight-bold">$3.99</span>
                </div>
                <div class="d-flex justify-content-between align-items-center mt-2">
                    <div class="ratings"> <i class="fa fa-star">
                    </i> <span>4.5</span> </div>
                  
                </div>
               <Link to="/payment"> <div class="mt-3"> <button class="btn btn-danger btn-block">Buy Now</button> </div></Link>
            </div>
        </div>
    </div>
     </div>
   </div>
 </div>
 
 {#if showModal}
	<Modal on:close="{() => showModal = false}">
		<h2 slot="header">
			modal
			<small><em>adjective</em>  mod·al \ˈmō-dəl\</small>
		</h2>

		<ol class="definition-list">
			<li>of or relating to modality in logic</li>
			<li>containing provisions as to the mode of procedure or the manner of taking effect —used of a contract or legacy</li>
			<li>of or relating to a musical mode</li>
			<li>of or relating to structure as opposed to substance</li>
			<li>of, relating to, or constituting a grammatical form or category characteristically indicating predication</li>
			<li>of or relating to a statistical mode</li>
		</ol>
		<a href="https://www.merriam-webster.com/dictionary/modal">merriam-webster.com</a>
	</Modal>
{/if}