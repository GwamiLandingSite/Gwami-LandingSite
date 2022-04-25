<template>
<nav class="navbar navbar-expand-lg navbar-light bg-transparent">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">
      <span class="mx-auto">
            <img class="img-fluid nav-logo"
              src="../assets/NavBar/Gwami-Logo-Side-Green-7-1.svg"
            />
      </span>  
    </a>
    <button class="navbar-toggler custom-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav ms-auto mb-2 mb-lg-0 ">
        <li class="nav-item">
          <a class="nav-link" aria-current="page" href="#Products">Products</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" aria-current="page" href="#Team">Team</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" aria-current="page" href="#Partners">Partners</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" aria-current="page" href="#KlimaEcosystem">Klima Ecosystem</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" aria-current="page" href="#ContactUs">Contact Us</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
</template>

<script>
export default {
  name: "NavBar",
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.navbar-brand{
  padding-left:17%;
}

.navbar-nav{
  padding-right:13%;
}

.navbar-light .navbar-nav .nav-link {
  color: #6D9032;
  font-family:'OpenSans', sans-serif;
  font-weight: 700;
  font-size:16px;
}

.navbar-toggler {
  color: #6D9032;
  border-color: #6D9032;
}

.custom-toggler .navbar-toggler-icon {
  background-image: url("data:image/svg+xml;charset=utf8,%3Csvg viewBox='0 0 32 32' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath stroke='rgba(109,144,50, 0.75)' stroke-width='2' stroke-linecap='round' stroke-miterlimit='10' d='M4 8h24M4 16h24M4 24h24'/%3E%3C/svg%3E");
}


@media only screen and (max-width: 767px) {
  .navbar .navbar-nav{
    padding-right:0%;
  }
}


</style>
