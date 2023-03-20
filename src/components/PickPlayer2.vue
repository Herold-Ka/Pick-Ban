<template>
    <div class="player2">
        <div class="playerEquipe1">
            <!--<img :src="`${team1[1]}`" alt="" v-for="team1 in player2.team1" :key="team1">-->
        </div>
        <div class="playerEquipe2">
        <!--<img :src="`${team1[1]}`" alt="" v-for="team1 in player2.team1" :key="team1">-->
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
    *{
        margin: 0;
    }
    .player2{
        height: 510px;
        width: 60px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }
    .playerEquipe1, .playerEquipe2{
        height: 240px;
        background-color: #FEFEFE;
        width: 60px;
        border: solid 1px #A0D2EC;
        outline: solid 0.1px black;
        outline-offset: -5px;
    }
</style>