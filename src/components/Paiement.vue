<template>

    <div class="ctn">
      <div class="nom_prenom">
        <input type="text" placeholder="Nom prenom" v-model="paiement.nom">
        <input type="text" placeholder="Numero de carte" v-model="paiement.numero">
      </div>
      <div class="cvv_exp">
        <input type="text" placeholder="CVV" v-model="paiement.cvv">
        <input type="text" placeholder="Date exp." v-model="paiement.date">
      </div>
      <button @click="test">envoi bb</button>

    </div>

</template>

<script>
    export default {
        data(){
          return {

            paiement : [
              {nom:'',numero:'', cvv: '' ,date: ''}
            ]

          }

        },
      methods:{
        test : function() {
          console.log(this.paiement)
        }

      }
    }
</script>

<style scoped>
  .ctn{display: flex;flex-direction: column;}
  .nom_prenom{display: flex;flex-direction: column;}
  .cvv_exp{display: flex;flex-direction: row;}
  .ctn{width: 400px;margin-top: 50px;}
</style>
