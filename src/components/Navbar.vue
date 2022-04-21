<template>
  <nav class="navbar sticky-top navbar-expand-lg navbar-light">
    <div class="container-fluid">
      <router-link to="/" class="navbar-brand">
        <img src="../assets/LOGO.png" alt="KlimaDAO Name Service" height="88" width="249" class="d-inline-block align-bottom navbar-img">
      </router-link>


      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>


      <div class="collapse navbar-collapse" id="navbarSupportedContent">

        <div class="d-flex ms-auto justify-content-left">

        <router-link v-if="isActivated && isNetworkSupported" to="/profile" class="navbar-text mx-4">Profile</router-link>
        <router-link to="/about" class="navbar-text mx-4">About KNS</router-link>
        <router-link to="/how" class="navbar-text mx-4">How it works</router-link>
        </div>
        
        <div class="d-flex ms-auto">

          <div v-if="isActivated" class="">
          
            <div class="btn-group mx-2">
              <button class="btn btn-Network btn-primary dropdown-toggle" type="button" id="dropdownMenuButton1" data-bs-toggle="dropdown" aria-expanded="false">
                {{getNetworkName}}
              </button>
              <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                <li>
                  <span 
                    class="dropdown-item" 
                    v-for="network in getSupportedNetworkNames"
                    @click="changeNetwork(network)"
                  >{{network}}</span>
                </li>
              </ul>
            </div>

            <div class="btn-group mx-2">
              <button class="btn btn-primary btn-Domain dropdown-toggle" type="button" id="dropdownMenuButton2" data-bs-toggle="dropdown" aria-expanded="false">
                {{ getNameOrAddress }}
              </button>
              <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton2">
                <router-link tag="li" class="dropdown-item" to="/profile">Profile</router-link>
                <router-link tag="li" class="dropdown-item" to="/">Buy domain</router-link>
                <router-link tag="li" class="dropdown-item" to="/search-domain">Search domain</router-link>
                <router-link tag="li" class="dropdown-item" to="/send-tokens">Send tokens</router-link>
                <router-link tag="li" class="dropdown-item" to="/about">About</router-link>
                <router-link tag="li" class="dropdown-item" to="/how">How it works</router-link>
                <router-link tag="li" class="dropdown-item" to="/browser">Browser extension</router-link>
                <li class="dropdown-item" @click="logout">Disconnect</li>
              </ul>
            </div>
          </div>

          <button v-else class="btn btn-primary btn-Disconnected" @click="open">Connect wallet</button>
        </div>

      </div>
    </div>
  </nav>
</template>

<script lang="ts">
import { mapGetters } from 'vuex';
import { useBoard, useEthers, useWallet } from 'vue-dapp';
import useChainHelpers from "../hooks/useChainHelpers";

export default {
  name: "Navbar",

  computed: {
    ...mapGetters("user", ["getUserShortAddress", "getUserSelectedName"]),
    ...mapGetters("network", ["getNetworkName", "getSupportedNetworks", "getSupportedNetworkNames", "isNetworkSupported"]),

    getNameOrAddress() {
      if (this.getUserSelectedName) {
        return this.getUserSelectedName;
      } else {
        return this.getUserShortAddress;
      }
    },

  },

  methods: {
    changeNetwork(networkName) {
      const networkData = this.switchNetwork(networkName); 

      window.ethereum.request({ 
        method: networkData.method, 
        params: networkData.params
      });
    },

    logout() {
      this.disconnect();
      localStorage.clear();
      localStorage.setItem("connected", "null");
    },

    openUrl(url) {
      window.open(url, '_blank').focus();
    }
  },
  
  setup() {
    const { open } = useBoard();
    const { disconnect } = useWallet();
    const { isActivated } = useEthers();
    const { switchNetwork } = useChainHelpers();

    return {
      isActivated, disconnect, open, switchNetwork
    }
  }
}
</script>

<style scoped>
.dropdown-item {
  cursor: pointer;
}
.navbar-brand {
  /*font-family: 'Cyber', cursive;*/
}
.navbar-light .navbar-brand .navbar-text {
  color: #232B2B;;
}

.navbar-text {
}
.navbar-light {
  background: #ffffff;
  border-radius: 0px 0px 13px 13px;
  padding: 10px;
  
}
.navbar-img {
  margin-right: 5px;
  color: #DBDFEA;
}

</style>
