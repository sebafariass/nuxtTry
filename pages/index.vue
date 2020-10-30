<template>
  <div class="container">
    <nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="https://bulma.io">
      <strong><h1>RICK AND MORTY</h1></strong>
    </a>

    <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div id="navbarBasicExample" class="navbar-menu">
    <div class="navbar-start">
      <a class="navbar-item">
        INICIO
      </a>

      <a class="navbar-item">
        DOCUMENTOS
      </a>

      <div class="navbar-item has-dropdown is-hoverable">
        <a class="navbar-link">
          MÁS
        </a>

        <div class="navbar-dropdown">
          <a class="navbar-item">
            Sobre
          </a>
          <a class="navbar-item">
            Nosotros
          </a>
          <a class="navbar-item">
            Contactanos
          </a>
          <hr class="navbar-divider">
          <a class="navbar-item">
            Reportanos!
          </a>
        </div>
      </div>
    </div>

    <div class="navbar-end">
      <div class="navbar-item">
        <div class="buttons">
          <a class="button is-primary">
            <strong>Sign up</strong>
          </a>
          <a class="button is-light">
            Log in
          </a>
        </div>
      </div>
    </div>
  </div>
</nav>
  <!-- card 1 --->
 <div class="columns">
    <div class="card column" v-for="(personaje,i) in personajes" :key="i">
  <div class="card-image">
    <figure class="image is-4by3">
      <img 
      :src="personaje.imagen">
    </figure>
  </div>
  <div class="card-content">
    <div class="media">
     
      <div class="media-content">
       
        <p class="subtitle is-6">{{personaje.nombre}}</p>
      </div>
    </div>

  
  </div>
</div>


 </div>
 
 <router-link to="/Otro">Ir a otra Web </router-link>
 

  </div>
</template>

<script>
export default {
  data() {
    return {
      personajes: [
{
id: 1,
nombre: 'Morty',
imagen: 'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
},
{
id: 2,
nombre: 'Rick',
imagen: 'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
},
{
id: 3,
nombre: 'Summer',
imagen: 'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
},
{
id: 4,
nombre: 'Beth',
imagen: 'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
},
{
id: 5,
nombre: 'Jerry',
imagen: 'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
}
]
    }
  }
}

</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
