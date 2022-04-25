<template>
  <section id="Products" class="PageTwo" 
      style="
        background-color:#485F1D;
        text-align:center;">
      <h1 class="product-page-title">
        <span class="text-dash-icon">
        <img src="../assets/PageTwo/Text-framer-emdash.svg"/>
        </span>
        Our Products
        <span class="text-dash-icon">
        <img src="../assets/PageTwo/Text-framer-emdash.svg"/>
        </span>
      </h1>
    <div class="container-fluid page-two-container" >
    <div class="row mb-5 mt-5">
      <div class="card col-12 col-lg-6 bg-transparent" 
          style="
                color:#FCFFF8;
                text-align:left;">
        <div class="card-body">
          <h1 class="block-titles">KlimaDAO Name Service (KNS)</h1>
          <p>KlimaDAO Name Service (KNS) is the world’s first regenerative domain that continuously offsets your carbon footprint and socially represents your carbon neutrality. KNS also enables users to map human readable names to blockchain and non-blockchain resources, like Ethereum addresses, IPFS hashes, or website URLs. </p>
          <button
          style="
          
          border-radius: 2px;
          border: 1px solid #CEE899;
          font-weight:bold;
          font-size:16px;
          height:54px;
          width: 148px;
          color:#485F1D;
          background:#CEE899;
          ">
          <a href="https://www.kns.earth">
          View KNS
          </a>
          </button>
          
        </div>
      </div>
      <div class="card col-12 col-lg-6 d-flex
                  justify-content-center bg-transparent mt-0">
        <img class="img-fluid" width="495" src="../assets/PageTwo/SampleKlimaDomains.svg"/>
      </div>
    </div>
    <div class="row" style="padding-bottom:100px;">
      <div class="card col-12 col-lg-6
            d-flex
            justify-content-start
            text-start
            bg-transparent">
        <h1 class="block-titles ">TerraNeutral Platform</h1>
        <p>A social platform for Refi, suitable for both individuals
          and businesses
        </p>
      </div>
      <div class="card coming-soon col-12 col-lg-6
              d-flex
              justify-content-star
              text-start
              bg-transparent
              product-page-title" 
            style="
              padding-top: 35px;
              color:#FCFFF8;">
        <h1 style="vertical-align:middle; ">Coming Soon</h1>
      </div>
    </div>
    </div>
  </section>
</template>

<script>
export default {
    name: "CardTwo"
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

a{
  text-decoration:none;
  color: inherit;
  font-size: inherit;
  font-weight: inherit;
}

p {
    color:#FCFFF8;
    margin-top:51px;
    font-size:20px;
}

h1, h2, h3, h4, h5, h6
{
    color:#FCFFF8;
}

.product-page-title {
        color:#FCFFF8; 
        padding-top:70px; 
        font-size:36px;
}

.block-titles {
  font-size: 60px;
  overflow-wrap:normal;
}

.card {
  border: 1px;
}

.coming-soon{
  
  padding-left:120px;
}

.page-two-container{
  padding-left:187px;
  padding-right:187px;
}

@media only screen and (max-width: 992px and min-width:768px) {
.coming-soon{
  padding-left: 10px;
}
.page-two-container{
  padding-left:10px;
  padding-right:10px;
}
}

@media only screen and (max-width: 767px) {
.coming-soon{
  padding-left: 10px;
}
.page-two-container{
  padding-left:10px;
  padding-right:10px;
}

}
</style>
