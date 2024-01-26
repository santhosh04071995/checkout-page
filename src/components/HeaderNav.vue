<template>
   
        
        <nav class="navbar navbar-dark bg-primary ">
        <div class="container-fluid bg-primary ">
          <img src="@/assets/logo.png" alt="" >
        <div class="d-flex justify-content-between align-items-baseline logs ">
                  <p class="hidden" style="font-size:12px"> Track Order </p>
                  <p class="hidden" style="margin:0px 0px 0px 3px">|</p>
                  <p><i class="fa fa-search" style="margin:0px 4px 0px 4px"></i> | </p> 
                  <p><img src="@/assets/user.png" alt="" >|</p>
                  <p><img src="@/assets/shopping.png" alt="" ></p>

        </div>
        </div>
    </nav>
    <!--tracker-->
    <div class="myshopping container mt-3">
      
      <div class="d-flex justify-content-between">

      
      <div class="shooping">
          <svg xmlns="http://www.w3.org/2000/svg" height="16" width="16" viewBox="0 0 512 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M464 256A208 208 0 1 0 48 256a208 208 0 1 0 416 0zM0 256a256 256 0 1 1 512 0A256 256 0 1 1 0 256zm256-96a96 96 0 1 1 0 192 96 96 0 1 1 0-192z"/></svg>
          <p>SHOOPING CART</p>
      </div>
      <div><svg xmlns="http://www.w3.org/2000/svg" height="16" width="16" viewBox="0 0 512 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M406.6 374.6l96-96c12.5-12.5 12.5-32.8 0-45.3l-96-96c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L402.7 224l-293.5 0 41.4-41.4c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-96 96c-12.5 12.5-12.5 32.8 0 45.3l96 96c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L109.3 288l293.5 0-41.4 41.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0z"/></svg></div>
      <div class="shooping">
          <svg xmlns="http://www.w3.org/2000/svg" height="16" width="16" viewBox="0 0 512 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8z"/></svg>
          <p >ORDER DETAILS</p>
      </div>
      <div><svg xmlns="http://www.w3.org/2000/svg" height="16" width="16" viewBox="0 0 512 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M406.6 374.6l96-96c12.5-12.5 12.5-32.8 0-45.3l-96-96c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L402.7 224l-293.5 0 41.4-41.4c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-96 96c-12.5 12.5-12.5 32.8 0 45.3l96 96c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L109.3 288l293.5 0-41.4 41.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0z"/></svg></div>
      <div class="shooping">
          <svg xmlns="http://www.w3.org/2000/svg" height="16" width="16" viewBox="0 0 512 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8z"/></svg>
          <p >MAKE PAYMENT</p>
      </div>
      
      </div><!--wholetrack-->
    </div><!--myshopping-->
  
  <!--Shooping cart-->
  <div class="shooping_cart container mt-4">
   <svg xmlns="http://www.w3.org/2000/svg" height="16" width="14" viewBox="0 0 448 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l160 160c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L109.2 288 416 288c17.7 0 32-14.3 32-32s-14.3-32-32-32l-306.7 0L214.6 118.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-160 160z"/></svg>
    <a href="#">SHOPPING CART</a>
    <hr>
  </div>
  
</template>

<script>
    export default {
        name: 'HeaderNav'
        
    }
</script>

<style scoped>
.shooping_cart > a {
  text-decoration: none;
  color: black;
  margin-left: 5px;
}
@media(min-width: 768px){
  .shooping_cart {
    display: none;
  }
}
.shooping {
  width: 500px;
  text-align: center;
}
.shooping > p {
  font-size: 10px;
}

.logs > p {
     font-style: Montserrat;
     margin-bottom: 0px !important;
     color: white;
  }
  @media (max-width : 766px){
    .hidden {
      display: none;
    }
    .myshopping {
      display: none;
    }

    
  }


</style>