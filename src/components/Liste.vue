<template>
  <div class="listePerso">
    <div class="card" style="width: 75px; height: 75px!important; " 
         v-for="perso in perso" :key="perso.id" v-show="perso.rarity === 0">
        <img class="card-img-top" :src="`${perso.img}`" alt="Card image cap" style="width: 72px; cursor: pointer; margin: auto;" v-on:click="pick(perso.id)">  
    </div>
  </div>
</template>

<script>
import listPerso from './listPerso';
export default {
    data(){
        return{
            perso: listPerso.arrayPersos,
             player1:{
                 team1:[],
                 team2:[],
             },
             player2:{
                 team1:[],
                 team2:[],
             },
             player1Pick: 0,
             player2Pick: 0,
        }
    },
    methods: {
        team: function(){

        },
        
    },
}
</script>

<style scoped>
    .listePerso{
        display: flex;
        flex-wrap: wrap;
        width: 840px;
        height: 440px;
        border: solid 1px green;
        background-color: rgba(230, 239, 242, 0.75);
        padding: 5px;
    }
    .card{
        margin: auto;
        background-color: #9B72AE;
        display: flex;
        align-items: center;
    }
    img{
        display: block;
        margin: auto;

    }
</style>