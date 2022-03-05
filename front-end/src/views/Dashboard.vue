<template>
<body>
  <div class="container-fluid">
    <div class="container-fluid hero-image">
      <div class="hero-text col-xs-12 col-sm-12 col-md-8 col-lg-6">
        <h2><strong>Amigo não se compra</strong></h2> 
        <strong>
          <p class="text-justify">A adoção é um ato de amor e responsabilidade. 
          Para adotar, basta se comprometer com um bichinho que dependerá sempre de você, cuidar dele, 
          dar afeto e um lar seguro. O amor é uma obrigação para adotar um coração.
          </p> 
        </strong>
      </div>
  </div>
  <div class="container">
    <div class="row">
      <div class="col">
        <strong>
          <h2 >Adote um amigo</h2>
        </strong>
            <p class="text-justify">
              Adotar é salvar vidas! Ter um animalzinho de estimação é ter uma amizade 
              verdadeira e leal. Animais conseguem nos amar com pureza e livre de julgamentos,
              mesmo nos momentos mais difíceis. Adotar um animal é adotar um amigo! 
            </p>
      </div>
    </div>
  </div>
    
    <div class="container">
    <div class="row row-cols-1 row-cols-md-3 g-3" >
      <div class="col" v-for="item in pets" :key="item.id">   
        <div class="card" >
          <router-link to="/gerenciamento-de-adotantes/novo">
            <img class="card-img-top" :src="item.logo" alt="" height="200" width="200">
          </router-link>
          <div class="card-body">
            <h5 class="card-title text-center">{{item.name}}</h5>
            <p class="text text-center">{{item.species}} | {{item.sex}} | {{item.age}} | Porte: {{item.size}}</p>
        </div>
        <div class="link text-center">
          <router-link to="/gerenciamento-de-adotantes/novo">
            <p>ADOTE</p>
          </router-link>
        </div>
      </div>
    </div>
    </div>
  </div>
  </div>
</body>
</template>
<script>

import PetMixin from '../mixins/pet-mixin';

export default {
  name: "Dashboard",
  mixins:[PetMixin],
  components: {
  },

  data() {
    return {
    };
  },

};
</script>
<style scope>
body {
  margin: 0;
}
.hero-image {
  background-image: url(~@/assets/images/dog.jpg);
  background-color: #020202; /* Used if the image is unavailable */
  height: 500px; /* You must set a specified height */
  background-position: center; /* Center the image */
  background-repeat: no-repeat; /* Do not repeat the image */
  background-size: cover; /* Resize the background image to cover the entire container */
}

.container-fluid {
  padding-right: unset;
  padding-left: unset;
}

.container, .container-lg, .container-md, .container-sm {
    max-width: 960px;
    margin-top: 40px;
}

.hero-text {
  position: absolute;
  padding-left: 50px;
  margin-top: 140px;
  color: white;
  font-family: Arial, Helvetica, sans-serif;
}

p{
  font-size: 20px;
  font-family: Arial, Helvetica, sans-serif;
}

.title{
  color: white;
}

.text{
  font-size: 18px;
}

.card{
  transition-duration:1s;
  transform-origin: 0% 0%
}

.card:hover{
  transform:scale(1.008);
}

a{
  text-decoration: none;
  color:rgb(18, 18, 19);
}
a:hover {
    text-decoration:none;
    color: #090753;
}
  
</style>
