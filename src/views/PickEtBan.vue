<template>
    <div class="divPickEtBan">
        <!--Decoration haute de la page-->
        <div class="decordHaut">
            <div class="firstDecor"></div>
            <div class="secondDecor"></div>
            <div class="thirdDecor"></div>
            <div class="fourthDecor"></div>
            <div class="thirdDecor"></div>
            <div class="secondDecor"></div>
            <div class="firstDecor"></div>
        </div>
        <!--Ban: Liste de personnage de banni-->
        <Ban />
        <!--Div Pick player & Liste des personnage-->
        <div class="containerPick">
            <!--Pick Player 1 -->
            <PickPlayer1/>
            <!--Liste des personnage-->
            <div class="listePerso">
                <div class="buttonRariry">
                    <button class="button4Star">4*</button>
                    <button class="button5Star">5*</button>
                </div>
                <div class="liste">
                    <Liste/>
                </div>
            </div>
            
            <!--Pick Player 2-->
            <PickPlayer2/>
            
        </div>
            <!--Decoration pied de page-->
        <div class="decordBas">
            <div class="firstDecor"></div>
            <div class="secondDecor"></div>
            <div class="thirdDecor"></div>
            <div class="fourthDecor"></div>
            <div class="thirdDecor"></div>
            <div class="secondDecor"></div>
            <div class="firstDecor"></div>
        </div>
    </div>
 </template>
 
 <script>
 import Ban from '../components/Ban.vue';
 import PickPlayer1 from '../components/PickPlayer1.vue';
 import Liste from '../components/Liste.vue';
 import PickPlayer2 from '../components/PickPlayer2.vue';
 export default {
    data(){
        return{
            Ban,
            PickPlayer1,
            Liste,
            PickPlayer2,
        }
    },
    components:{
        Ban,
        PickPlayer1,
        Liste,
        PickPlayer2,
    },
    methods: {
         
    },

     
 }

 </script>
 
 <style scoped>
 *{
     margin: 0;
 }
 .divPickEtBan{
     background-image: url("./img/other/genshin-impact-sumeru-4.png");
     background-size: cover;
     width: 100%;
     margin: 0;
     padding: 0;
     height: 100vh;
 }
 /***Décord du haut */
 .decordHaut{
     width: 90vw;
     height: 60px;
     margin: auto;
     display: flex;
     justify-content: space-between;
     align-items: center;
 }
 .decordBas{
     width: 90vw;
     height: 60px;
     margin: auto;
     display: flex;
     justify-content: space-between;
     align-items: center;
 }
 .firstDecor{
     height: 8px;
     width: 450px;
     background-color: white;
     border-radius: 1px;
 }
 .secondDecor{
     height: 11px;
     width: 50px;
     background-color: white;
     border-radius: 1px;
 }
 .thirdDecor{
     height: 15px;
     width: 50px;
     background-color: white;
     border-radius: 1px;
 }
 .fourthDecor{
     height: 15px;
     width: 15px;
     border: solid 7px white;
     border-radius: 1px;
 }
 /**Container Pick */
 .containerPick{
    width: 1250px;
    height: 530px;
    border: solid 1px black;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
 }
 .listePerso{
    display: flex;
 }
 .buttonRariry{
    display: flex;
    flex-direction: column;
 }
 .buttonRariry button{ 
    border: none;
    height: 30px;
    width: 40px;
    margin-bottom: 1px;
    cursor: pointer;
    border-radius: 2px 0 0 2px;
    color: white;
 }
 .button4Star{
    background-color: #9BA5E6;
 }
 .button5Star{
    background-color: #FF966D;
 }
 </style>