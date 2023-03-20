<template>
  <div class="ban">
        <div class="player1Pseudo">
            <p>joueur</p>
            <h1>player1</h1>
        </div>
        <div class="banPlayer1"></div>
        <div class="chrono"></div>
        <div class="banPlayer2"></div>
        <div class="player2Pseudo">
            <p>joueur</p>
            <h1>player2</h1>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
    @import url('https://fonts.cdnfonts.com/css/myriad-pro');
    *{
        margin: 0;
    }
    /*Ban */
    .ban{
        width: 1300px;
        height: 60px;
        display: flex;
        justify-content: space-between;
        margin: auto;
    }
    .player1Pseudo, .player2Pseudo{
        background-color: #FFFFFF;
        border: solid 1.5px #6E8DF9;
        width: 120px;
        height: 45px;
        align-self: flex-end;
    }
    .player1Pseudo > h1, .player1Pseudo > p,.player2Pseudo > h1, .player2Pseudo > p{
        font-family: 'Myriad Pro', sans-serif;
        font-size: 12px;
        text-align: center;
        margin: auto;
    }
    .banPlayer1, .banPlayer2{
        background-color: rgba(174, 125, 131, 0.7);
        width: 310px;
        height: 60px;
    }
    .chrono{
        width: 100px;
        height: 60px;
        background-color: #FEFFFD;
    }
</style>