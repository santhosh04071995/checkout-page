<template>
    <div class="main container-fluid pb-4"> 
        
            <div class="discount container bg-warning text-center">
                <p >shop for $5000 or more and get 10% discount on your order</p>
            </div><!--container-->

            <div class="cart container mt-2 mb-4">
                 <h4>Shopping cart</h4>
            </div>

            <div class="cartitem container bg-white">
                <div class="row m-2">
                    <div class="header col-6 col-md-6 col-lg-6">
                        <p>Product</p>
                    </div>
                    <div class="col-3 col-md-2 col-lg-2">
                        <p>Price</p>
                    </div>
                    <div class="col-3 col-md-2 col-lg-2">
                        <p>Quantity</p>
                    </div>
                    <div class="subtotal col-md-2 col-lg-2">
                        <p>Subtotal</p>
                    </div>
                </div><!--row-->
                <hr>
             <div v-for="(pro,index) in myuser.products" :key="pro">
            <div class="row d-flex align-items-center">
               
                    <div class="col-6 col-md-6 col-lg-6">
                            <div class="d-flex">
                                <div class="imgbox">
                                    <img src="@/assets/phone.png" alt="" style="">
                                </div><!--imagdiv-->
                                <div style="margin-left:3px"><!--name,price,desc-->
                                    <p style="background:darkblue;color:white;display:inline;font-weight:bold;">{{pro.tagline}}</p>
                                    <p style="color:black">{{pro.name}}</p>
                                    <p style="width:100px">{{pro.desc}}</p>
                                </div><!--name,price,desc-->
                            </div><!--productflex-->
                    </div><!--col-6 col-md-6 col-lg-6-->
                    
                    <div class="col-3 col-md-2 col-lg-2">
                        <p>{{pro.price}}$</p>
                    </div>
                    <div class="col-3 col-md-2 col-lg-2">
                        <div class="quantity d-flex ms-auto">
                            <img @click="decre(pro)" src="@/assets/minus-active.png" alt="">
                                <div class="border w-10">
                                    <p>{{pro.quantity}}</p> 
                                </div>
                               <img @click="incre(pro)"  src="@/assets/plus.png" alt="">
                       </div><!--quantity-->
                    </div>
                    <div class="subtotal col-md-2 col-lg-2 ">
                        <div class="d-flex">
                            <p>{{pro.total}}$</p>
                            <img @click="del(index)" src="@/assets/DELETE.png" alt="">
                        </div>    
                    </div>
               
                </div><!--row-->    
            </div><!--key-->

            
            

    <div class="addrsum container  mt-4">    <!--address and summary-->
            <div class="address">
                <h5>Delivery Availability</h5>
                    
                    
                    <form>     
                        
                            <div class="d-inline-flex">
                                
                                <div><img src="@/assets/LOCATION.png" alt="">
                                <input type="text" v-model="pin"></div>
                                <p class="text-primary font-weight-bold text-uppercase ml-4">change</p>
                            </div>
                            <hr class="w-15">
                            <div class="d-flex ">
                                <div v-show="pin=='560066'">
                                    <div class="w-25 text-center"> 
                                    <img src="@/assets/check.png" alt="" class="kk">
                                    
                                        <p v-if="myuser.pincode['560066']['deliveryPrice']!=0">{{myuser.pincode['560066']['deliveryPrice']}} Delivery Charges</p>
                                        <p v-else-if="myuser.pincode['560066']['deliveryPrice']==0">Free delivery</p>
                                    </div><!--delivery charge and free delivery-->
                                </div><!--pin-->

                                <div v-show="pin=='560066'">
                                    <div class="w-50 text-center ">
                                    <img src="@/assets/check.png" alt="">
                                        <p v-if="myuser.pincode['560066']['cashOnDelivery']==false">Cash on delivery not available</p>
                                        <p v-if="myuser.pincode['560066']['cashOnDelivery']==true">Cash on delivery</p>
                                    </div><!--delivery charge and free delivery-->
                                </div><!--pin-->

                                <div v-show="pin=='560066'">
                                    <div class="w-50 text-center">    
                                    <img src="@/assets/check.png" alt="">
                                    
                                        <p>Estimated delivery delivery time is
                                            {{myuser.pincode['560066']['estimatedDays']['min']}}
                                            -{{myuser.pincode['560066']['estimatedDays']['max']}} days
                                        </p>
                                    </div><!--delivery charge and free delivery-->
                                </div><!--pin-->
                            </div>

                            <div class="d-flex">
                                <div v-show="pin=='560067'">
                                    <div class="w-25 text-center"> 
                                    <img src="@/assets/check.png" alt="" class="kk">
                                    
                                        <p v-if="myuser.pincode['560067']['deliveryPrice']!=0">{{myuser.pincode['560067']['deliveryPrice']}}</p>
                                        <p v-else-if="myuser.pincode['560067']['deliveryPrice']==0">Free delivery</p>
                                    </div><!--delivery charge and free delivery-->
                                </div><!--pin-->

                                <div v-show="pin=='560067'">
                                    <div class="w-50 text-center ">
                                    <img src="@/assets/check.png" alt="">
                                        
                                        <p v-if="myuser.pincode['560067']['cashOnDelivery']==true">Cash on delivery</p>
                                    </div><!--delivery charge and free delivery-->
                                </div><!--pin-->

                                <div v-show="pin=='560067'">
                                    <div class="w-70 text-center">    
                                    <img src="@/assets/check.png" alt="">
                                    
                                        <p>Estimated delivery delivery time is
                                            {{myuser.pincode['560067']['estimatedDays']['min']}}
                                            -{{myuser.pincode['560067']['estimatedDays']['max']}} days
                                        </p>
                                    </div><!--delivery charge and free delivery-->
                                </div><!--pin-->
                            </div>

                            <div class="d-flex">
                                <div v-show="pin=='560068'">
                                    <div class="w-25 text-center"> 
                                    <img src="@/assets/check.png" alt="" class="kk">
                                    
                                        <p v-if="myuser.pincode['560068']['deliveryPrice']!=0">{{myuser.pincode['560068']['deliveryPrice']}} Delivery Charges</p>
                                        <p v-else-if="myuser.pincode['560068']['deliveryPrice']==0">Free delivery</p>
                                    </div><!--delivery charge and free delivery-->
                                </div><!--pin-->

                                <div v-show="pin=='560068'">
                                    <div class="w-50 text-center ">
                                    <img src="@/assets/check.png" alt="">
                                        <p v-if="myuser.pincode['560068']['cashOnDelivery']==false">Cash on delivery not available</p>
                                        <p v-if="myuser.pincode['560068']['cashOnDelivery']==true">Cash on delivery</p>
                                    </div><!--delivery charge and free delivery-->
                                </div><!--pin-->

                                <div v-show="pin=='560068'">
                                    <div class="w-70 text-center">    
                                    <img src="@/assets/check.png" alt="">
                                    
                                        <p>Estimated delivery delivery time is
                                            {{myuser.pincode['560068']['estimatedDays']['min']}}
                                            -{{myuser.pincode['560068']['estimatedDays']['max']}} days
                                        </p>
                                    </div><!--delivery charge and free delivery-->
                                </div><!--pin-->
                            </div>

                        <!-- </div>  -->
                        <!-- <p class="text-primary font-weight-bold text-uppercase">change</p> -->
                    </form>
                
        </div>
        <div class="summary pb-4">
                <h5><strong>Order Summary({{Procount}} items) </strong></h5>
            <div class="GrandTotal d-flex justify-content-between">
                <p>Subtotal</p>
                <p>{{GrandTotal}}</p>
            </div>
            <div v-if="discount" class="discount d-flex justify-content-between">
                <p>Total Discount</p>
                <p>{{myuser.discount.discountPercentage}}</p>
            </div>
            <div class="shipping d-flex justify-content-between">
                <p>Standard Shipping</p>
                <p>Free</p>
            </div>
                <div class="d-flex justify-content-between align-items-center  mt-4" >
                <p class=" display-6 font-weight-bold">GrandTotal</p>
                <h5 class="display-6 me-4"><strong>{{final}}$</strong></h5>
            </div>
            <div class="continue d-flex justify-content-between align-items-baseline mt-4" >
                <p class="text-uppercase fw-bolder text-primary pb-2">continue shopping</p>
            <a href="#" class="btn btn-primary btn active text-uppercase rounded-pill me-4" role="button" aria-pressed="true">checkout</a>
            </div>
        </div>
    </div>
    
    </div><!--container-->
        </div><!--container-fluid-->
    
</template>
<script>
    import jsonuser from '../assets/user.json'
    export default {
        name : 'ContentSec',
        data() {
            return {
                myuser : jsonuser,
                pin: '',
            }
        },
        methods: {
            del(index)
            {
                this.myuser.products.splice(index,1)
            },
           incre(x){
            if(x.quantity < 5)
            {
                x.quantity++;
                x.total = x.price*x.quantity;
            }
            else{
                alert('Out Of Stock');
            }
           },
           decre(x){
            if(x.quantity==0)
             {
                alert('Quantity is 0')
             }
             else {
                x.quantity--;
                x.total= x.price*x.quantity;

             }
           },
            mydisable() {
               this.myuser.products[0].style.background="red";
                
            }
        },
        computed: {
            GrandTotal() {
                let sum=0;
               for(let i=0; i<this.myuser.products.length; i++)
               {
               sum += this.myuser.products[i].total;
               }
               
                return sum;
            },
            Procount() {
             let count =  this.myuser.products.length;
                return count;
            },
            discount() {    ////myuser.discount.minTotal
                if(this.GrandTotal> this.myuser.discount.minTotal)
                return true;
            else
                return false;
            },
            final() {
                let k = this.GrandTotal-this.discount
                return Intl.NumberFormat('en-US').format(k);
                 
            },
           
        }

       
    }
</script>
<style scoped>
input[type=text] {
    background: transparent;
    border: none;
    border-bottom: 1px solid #000000;
}
 .imgbox  img {
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-top: 10px;
}
.imgbox {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    width: 100px;
    height: 100px;
}

p{
    margin-bottom: 0px;
    font-family: 'Montserrat';
    font-size: 16px; 
}

.cartitem {
    min-height: 500px;
    border: 2px solid lightslategray;
}
.cart > p {
    font-size: 25px;
    /* font-style: Montserrat; */
}
.main {
    background: rgb(241 247 251);
    min-height: 700px;
}
@media(max-width: 766px)
{
    .discount,.subtotal {
        display: none;
    }
    .continue {
        display: block !important;
        text-align: center;
    }
    .shipping,.discount{
        margin-top: 30px !important;
    }

    
}
@media(min-width: 768px){
    .addrsum {
        display: flex;
        justify-content: space-between;
    }
    
}
</style>