<template>
  <section id="Intro" class="intro-Page" style="background-color:#F3FCE2;
  text-align:center;" >
    <NavBar/>

    <div class="row" style="height:675px;">
      <div class="col-3" 
      style="
      height: 675px;
      padding-left: 0;
      padding-bottom:0;
      position:relative;">
        <img class="img-fluid leaves-left" src="../assets/PageOne/Leaves-Pg1-Left.svg"/>
      </div>
      <div class="col-6" style="height:675px;">
        <h1 class="intro-title">
          Products for climate action
        </h1>
        <p class="intro-body">
        Gwami Labs is focused on building a suite of blockchain 
        and web2 based products on the refi ecosytem. 
        The goal is to make Climate Action the only option 
        through accessibility, incentives, social culture, 
        education and amplification.</p>
        <div>
        <span class="PageOneLegend">Unlock Refi</span>
        <span class=" mx-3 PageOneLeafIcon">
          <img src="../assets/PageOne/Green-Leaf-2.svg"/>
        </span>
        <span class="PageOneLegend">Build on KlimaDAO</span>
        </div>
        <div>
        <span class="PageOneLegend">Collaborate globally</span>
        <span class=" mx-3 PageOneLeafIcon">
          <img src="../assets/PageOne/Green-Leaf-2.svg"/>
        </span>
        <span class="PageOneLegend">Promote climate action</span>
        </div>
      </div>
      <div class="col-3" 
          style="
          padding-left:0;
          padding-right: 0;
          padding-top: 0;
          padding-bottom: 0;
          height: 675px;
          position:relative;">
        <img class="img-fluid leaves-right" src="../assets/PageOne/Leaves-Pg1-Right.svg"/>
      </div>
    </div>
  </section>
</template>

<script>
import NavBar from "./NavBar.vue";
export default {
    name: "CardOne",
    components: { NavBar }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

p {
    color:#304010;
    margin-top:51px;
    font-size:20px;
}

h1, h2, h3, h4, h5, h6
{
    color:#304010;
}

h1 {
  margin-top:17.6%;
  font-size:72px;
}

.PageOneLegend{
    font-family: 'Frank Ruhl Libre', serif;
    font-weight: 700;
    font-size :24px;
    color:#304010;
}


.leaves-left{
  display:block;
  position:absolute;
  left:0px;
  bottom:0px;

}

.leaves-right{
  display:block;
  position:absolute;
  right: 0px;
  bottom: 0px;
}

@media only screen and (max-width: 767px and min-width:401px) {

  h1 {
    margin-top:55px;
    font-size:62px;
  }
  p {
    font-size:16px;
  }
  .PageOneLegend {
    font-size:14px;
    white-space: nowrap;
  }

  .leaves-left {
  display:block;
  position:absolute;
  left:0px;
  bottom:105px;
  }

  .leaves-right{
  display:block;
  position:absolute;
  right: 0px;
  bottom: 105px;
  }

}

@media only screen and (max-width: 400px) {

  h1 {
    margin-top:28px;
    font-size:42px;
  }
  p {
    margin-top: 20px;
    font-size:14px;
  }
  .PageOneLegend {
    font-size:12px;
    white-space: nowrap;
    text-align: left;
  }

  .leaves-left {
  display:block;
  position:absolute;
  left:0px;
  bottom:55px;
  }

  .leaves-right{
  display:block;
  position:absolute;
  right: 0px;
  bottom: 55px;
  }

}


</style>
