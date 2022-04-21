<template>
  <div class="container-fluid text-center mt-3">

    <a target="_blank" href="https://www.klimadao.finance/">Built for KlimaDAO</a>
    
    <span> | </span>

    <a target="_blank" href="https://twitter.com/gwamilabs">by GwamiLabs</a>

    <span> | </span>

    <a target="_blank" href="https://twitter.com/punkdomains">powered by Punk Domains</a>
    
  </div>

  <div class="container-fluid text-center">

    <a class="icons" target="_blank" href="https://github.com/GwamiLabs"><i class="bi bi-github"></i></a>

    <a class="icons" target="_blank" href="https://discord.gg/gwamilabs"><i class="bi bi-discord"></i></a>

    <a class="icons" target="_blank" href="https://twitter.com/gwamilabs"><i class="bi bi-twitter"></i></a>
    
  </div>
</template>

<script>
import { useEthers } from 'vue-dapp';
import { mapGetters } from 'vuex';

export default {
  name: "Footer",

  computed: {
    ...mapGetters("network", ["isNetworkSupported"]),
    
  },

  setup() {
    const { isActivated } = useEthers()
    return { isActivated }
  },
}
</script>

<style scoped>
a {
  text-decoration: none;
  color: #232B2B;
}

a:hover {
  text-decoration: underline;
  color: #232B2B;
}

.container-fluid {
  /*background-color: #24263A;*/
  background-color: transparent;
  padding: 20px 0px;
  border-radius: 10px;
}

.icons {
  margin-left: 15px;
  margin-right: 15px;
  font-size: 2em;
  color: #232B2B;
}

.polygon {
  vertical-align: text-bottom;
  width: 40px;
}

.polygon svg circle {
  fill: #DBDFEA;
}

.polygon:hover svg circle {
  fill: white;
}
</style>