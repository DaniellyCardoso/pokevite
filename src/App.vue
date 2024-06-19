<script setup>
import { ref } from 'vue'

let num = ref(0)

</script>

<template>
  <!-- Navbar-->
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <routerLink class="navbar-brand" to="/">
        <img src="https://cdn-icons-png.flaticon.com/512/188/188987.png" alt="" width="30" height="24"
          class="d-inline-block align-text-top">
        PokeVite
      </routerLink>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
        aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <routerLink class="nav-link " aria-current="page" to="/">Home</routerLink>
          </li>
          <li class="nav-item">
            <routerLink class="nav-link" to="/about">About</routerLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Content -->

  <div class="main">
    <router-view>

    </router-view>
  </div>

  <footer class="bg-dark text-light">
    <div>
      Design in {{ new Date().getFullYear() }}
    </div>
  </footer>
</template>

<style>
body{
  height: 100vh;
  background: rgb(4,0,255);
  background: linear-gradient(0deg, rgba(4,0,255,1) 0%, rgba(16,16,32,1) 85%); 
  
}
footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 56px;
}
</style>