<template>
  <div>
      <ul class="nav">
          <li class="btn btn-primary btn-nav"><router-link to="/" exact>Accueil</router-link></li>
          <li class="btn btn-primary btn-nav"><router-link to="/Page1">Page1</router-link></li>
          <li class="btn btn-primary btn-nav"><router-link to="/Page2">Page2</router-link></li>
      </ul>
  </div>
</template>

<script>


export default {
  name: 'Header',
  components: {
   
  }
}
</script>

<style>

.btn-nav {
margin: 5px;

}

.btn-nav a {
    color: #ffffff;
}
.btn-nav a:hover {
    color: #ffffff;
}
</style>
