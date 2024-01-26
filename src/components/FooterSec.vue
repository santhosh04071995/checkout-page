<template>
  <div class="fluid-container bg-dark">
    <div class="sponser container pt-4 row">
      <div class="lefter d-flex justify-content-evenly col-9">
        <div class="footer1">
          <h6 class="text-uppercase">lorem</h6>
          <p>Dummy</p>
          <p>Dummy</p>
          <p>Dummy</p>
          <p>Dummy</p>
        </div>
        <!--footer-->
        <div class="footer2">
          <h6 class="text-uppercase">lorem</h6>
          <p>Dummy Test</p>
          <p>Dummy Test</p>
          <p>Dummy Test</p>
          <p>Dummy Test</p>
          <p>Dummy Test</p>
          <p>Dummy Test</p>
        </div>
        <!--footer-->
        <div class="footer3">
          <h6 class="mydiv1 text-uppercase">lorem</h6>
          <p>Dummy Test</p>
          <p>Dummy Test</p>
          <p>Dummy Test</p>
          <p>Dummy Test</p>
          <p>Dummy Test</p>
        </div>
        <!--footer-->
        <div class="footer4">
          <h6 class="mydiv2 text-uppercase">lorem</h6>
          <p>Dummy</p>
          <p>Dummy</p>
          <p>Dummy</p>
          <p>Dummy</p>
          <p>Dummy</p>
          <p>Dummy</p>
        </div>
        <!--footer-->
      </div>
      <!--lefter-->

      <div class="righter col-3">
        <div class="vl"></div>
        <div class="me-2" style="width: 300px">
          <h6 class="text-uppercase">call us</h6>
          <div class="d-flex justify-content-between w-100">
            <div>
              <p>Monday-Friday</p>
              <p>8am to 9pm CST</p>
            </div>
            <div>
              <p>saturday & Sunday</p>
              <p>10AM to 6pm CST</p>
            </div>
          </div>
          <div class="d-flex">
            <img class="d-flex" src="@/assets/phone-logo.png" alt="" />
            <p>1800-123-123</p>
          </div>
          <hr style="border: 1px solid white" />
          <p>support.us@test.com</p>
        </div>
      </div>
    </div>
    <!--row-->

    <div class="myfooter container">
      <hr />
      <div class=" text-center text-md-start">
        <p>Dummy | Dummy | Dummy</p>
        <p>Lorem ipsum dolor sit amet consectetur.</p>
      </div>
    </div>
  </div>
  <!--container-fluid-->
</template>
<script>
export default {
  name: "FooterSec",
};
</script>

<style scoped>
@media (max-width: 767px) {
  .sponser {
    display: table-column-group;
  }
  .myfooter > hr {
    display: none;
  }

}
@media(max-width: 768px) {
    .footer3 {
        display: none;
    }
    .footer4 {
        display: none;
    }
    .sponser {
        margin-left: -100px;
    }
}
h6 {
  color: white;
}

p {
  font-family: "Montserrat";
  font-size: 12px;
  margin-bottom: 0px;
  color: rgba(255, 255, 255, 0.822);
}
.sec {
  padding-left: 30px;
}
.vl {
  border-left: 1px solid white;
  height: 150px;
  float: left;
}
hr {
  width: 100%;
  color: white;
}
</style>