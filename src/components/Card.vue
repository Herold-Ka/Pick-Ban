<template>
   <div class="divPickEtBan">
    <div class="playerPick">
        <section class="player1">
            <h2>player 1</h2>
            <div class="PlayerEquipe1">
                <img :src="`${team1[1]}`" alt="" v-for="team1 in player1.team1" :key="team1">
            </div>
        </section>
        <section class="perso" style="background-color: aquamarine;">
            <div class="card" style="width: 50px; height: 50px!important; border: solid 1px black;" v-for="perso in perso" :key="perso.id">
                <img class="card-img-top" :src="`${perso.img}`" alt="Card image cap" style="width: 35px; cursor: pointer;" v-on:click="pick(perso.id)">
                <div class="card-body">
                    <h5 class="card-title" style="color: black;">{{ perso.nom }}</h5>
                </div>
            </div>
        </section>
        <section class="player2">
            <h2>player 2</h2>
            <div class="PlayerEquipe1">
                <img :src="`${team1[1]}`" alt="" v-for="team1 in player2.team1" :key="team1">
            </div>
        </section>
    </div>
    
   </div>
</template>

<script>
import { createIfStatement } from "@vue/compiler-core"
import listPerso from "./listPerso"
export default {
    data(){
        return{
            perso: listPerso.perso,
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
            ponpon:[1,2,3]
        }
    },
    methods: {
        check: function(id){
            console.log(this.player1.team1.flat().includes(id))
            
            
        },
        team: function(id){
            this.check(id)
            if(this.player1.team1.flat().includes(id) || this.player2.team1.flat().includes(id)){
                console.log(`Personnage déjà selectionner`)
                alert('already use')
            }
            else if(this.player1Pick === 0 && this.player2Pick === 0){
                
                this.player1Pick ++

                this.player1.team1.push(new Array(id, this.perso[id - 1].img) )
                console.log(this.player1.team1 + 'player1')
            }
            else if(this.player1Pick > 0 && this.player2Pick === 0 || this.player2Pick === 1){
                this.player2Pick ++
                this.player2.team1.push(new Array(id, this.perso[id - 1].img) )
                console.log(this.player2.team1 + 'player2')
            }
            else if(this.player1Pick === 1 || this.player1Pick === 2 && this.player2Pick === 2){
                this.player1Pick ++
                this.player1.team1.push(new Array(id, this.perso[id - 1].img) )
                console.log(this.player1.team1 + 'player1')
            }
            else if(this.player2Pick === 2 || this.player2Pick === 3 && this.player1Pick === 3){
                this.player2Pick ++
                this.player2.team1.push(new Array(id, this.perso[id - 1].img) )
                console.log(this.player2.team1 + 'player2')
            }
            else if(this.player1Pick === 3 && this.player2Pick === 4){
                this.player1Pick ++
                this.player1.team1.push(new Array(id, this.perso[id - 1].img) )
                console.log(this.player1.team1 + 'player1')
            }
            else if(this.player1Pick === 4 && this.player2Pick === 4){
                console.log('fini')
                alert('les équipes sont complète')
            }
        },
        
        pick: function(id){
           this.team(id)      
        }
    },
    
}
console.log(listPerso);
</script>

<style scoped>
.playerPick{
    display: flex;
    justify-content: space-between;
    width: 100%;
}
.player1{
    width: 100px;
    background-color: blue;
}
.player2{
    width: 100px;
    background-color: aqua;
}
.perso{
    width: 700px;
    display: flex;
    flex-wrap: wrap;
}


</style>