<template>
  <section id="Team" class="Team-Page" 
          style="
          background-color:#FCFFF8;
          text-align:center;">
  <h1 class="team-page-title">
    <span>
      <img src="../assets/PageThree/Text-framer-emdash.svg"/>
    </span>
      Our Team
    <span>
      <img src="../assets/PageThree/Text-framer-emdash.svg"/>
    </span>
    
  </h1>
  <div class="container-fluid team-cards-holder">
  <div class="row mt-5 row-cols-3 align-items-center justify-content-center">
        <div class="card col">
          <div class="card-body">
              <img class="card-img-top" src="../assets/PageThree/TimmyKlima.svg"
              alt="image-photo"/>
              <h5 class="card-title">Timmy</h5>
              <span>Founder of Gwami and KlimaDAO contributor</span>
            <div class="card-twitter-icon">
              <a href="https://twitter.com/gwamilabs">
                  <TwitterBird />
              </a> 
            </div>
          </div>
        </div>
        <div class="card col">
          <div class="card-body">
              <img class="card-img-top" src="../assets/PageThree/Rajasmasala.svg" 
              alt="image-photo"/>
              <h5 class="card-title">Rajasmasala</h5>
              <span>Lead developer for Gwami</span>
            <div class="card-twitter-icon">
              <a href="https://twitter.com/gwamilabs">
                  <TwitterBird />
              </a> 
            </div>
              
          </div>
        </div>
        <div class="card col">
          <div class="card-body">
              <img class="card-img-top" src="../assets/PageThree/SlaptainShwirv.svg" 
              alt="image-photo"/>
              <h5 class="card-title">SlaptainShwirv</h5>
              <span>Community Lead for Gwami</span>
            <div class="card-twitter-icon">
              <a href="https://twitter.com/gwamilabs">
                  <TwitterBird />
              </a> 
            </div>
              
          </div>
        </div>
      <div class="card col">
        <div class="card-body">
            <img class="card-img-top" src="../assets/PageThree/Tigerlily.svg" 
            alt="image-photo"/>
            <h5 class="card-title">Tigerlily</h5>
            <span>Marketing lead for Gwami</span>
            <div class="card-twitter-icon">
              <a href="https://twitter.com/gwamilabs">
                  <TwitterBird />
              </a> 
            </div>
            
        </div>
      </div>
      <div class="card col">
        <div class="card-body">
            <img class="card-img-top" src="../assets/PageThree/Lell.svg" 
            alt="image-photo"/>
            <h5 class="card-title">Lell</h5>
            <span>Creative director for Gwami</span>
            <div class="card-twitter-icon">
              <a href="https://twitter.com/gwamilabs">
                  <TwitterBird />
              </a> 
            </div>   
        </div>
      </div>
      <div class="card col">
        <div class="card-body">
            <img class="card-img-top" src="../assets/PageThree/Sy-Zygy.svg" 
            alt="image-photo"/>
            <h5 class="card-title">Sy Zygy</h5>
            <span>Advisor to KlimaDAO, product lead of KlimaDAO</span>
            <div class="card-twitter-icon">
              <a href="https://twitter.com/gwamilabs">
                  <TwitterBird />
              </a> 
            </div>
        </div>
      </div>
    </div>
    </div>
  </section>
</template>

<script>
import TwitterBird from "./icons/TwitterBird.vue"
//import TeamMemberCard from "./TeamMemberCard.vue";
export default {
    name: "CardThree",
    components: { TwitterBird },
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.team-page-title {
        color:#202832; 
        padding-top:70px; 
        font-size:36px;
}

.card {
        margin: 32px; /* Added */
        float: center;
        margin-top: 71px;
        min-height:210px;
        width: 260px;
}

.card-img-top {
  height:37.6%;
  position:absolute;
  top: -18.8%;
  right:0.5%;
  left:0.5%;
  
}

.card-title {
  margin-top:43px;
}

.card-body {
  font-size: 16px;
  text-align:center;
}

.card-twitter-icon {
  margin-top:12px;
  padding-bottom:6px;

}

.team-cards-holder {
  padding-left: 115px;
  padding-right: 115px;
  padding-bottom:140px;
}

@media only screen and (max-width: 767px) {
  .card {
    height: 260px;
  }
}
</style>
