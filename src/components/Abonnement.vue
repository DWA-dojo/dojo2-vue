<template>
  <div class="container">
    <div>
      <div class="carte">
        <div v-for="item in abonnement">
          <h1>{{ item.nomAbonnement }}</h1>
          <h2>{{ item.prix }}</h2>
          <p>{{ item.option }}</p>
          <input type="radio" name="valide" v-model="resultat" >
        </div>

      </div>


    </div>
  </div>
</template>


<script>
    import axios from 'axios'

    export default {


        data (){
          return{
            abonnement: [
              {nomAbonnement:'Low cost', prix:'5',option :'Lorem ipsum'},
              {nomAbonnement:'Normale', prix:'10',option :'Lorem ipsum'},
              {nomAbonnement:'Vip', prix:'15',option :'Lorem ipsum'}
            ],
            resultat:null,
          }
        }


    }
</script>

<style scoped>
.carte{height: 100%;width: auto;display: flex;flex-direction: row;justify-content: center;}
.carte div{border: 1px solid black;width: 200px;}
.container{display: flex;flex-direction: column;align-items: center;}
.container input[type="button"]{width: 200px;height: 30px;margin-top: 30px;}
</style>
