<template>
<div class="hello">
    <div class="conteiner">
      <div class="item1">1</div>
      <div class="item2">2</div>
      <div class="item3">3</div>
      <div class="item2">4</div>
      <div class="item1">5</div>
    </div>
    <br><br><br><br><br><br>
    <div class="conteiner2">
      <div class="item1">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
      <div class="item">7</div>
      <div class="item">8</div>
      <div class="item2">9</div>
    </div>

    <br><br><br><br><br><br>
    <div class="conteinerBlue">
      <div class="conteinerYellow">
          <div class="conteinerRed">

          </div>
      </div>
    </div>


    <br><br><br><br><br><br>
    <div class="conteiner4">
      <div class="item">1</div>
      <div class="item1">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
    </div>
</div>
  </template>
  
  <script>
  export default {
    name: 'lab1Items',
    props: {
      msg: String
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
    .conteiner{
      display: flex;
      flex-flow: row wrap;
      justify-content: center;
    }

    .conteiner div {
      float: left;
      height: 30px;
      width: 30px;
      background: yellow;
      padding: 5px;
      margin-left: 10px;
    }

    .conteiner .item1 {
      margin-top: 100px;
    }

    .conteiner .item2 {
      margin-bottom: 50px;
      margin-top: 50px;
    }

    .conteiner .item3 {
      margin-bottom: 100px;
    }

    .conteiner2{
      width: 480px;
      display: flex;
      flex-flow: row wrap;
      justify-content: stretch;
    }

    .conteiner2 div {
      float: left;
      height: 30px;
      width: 30px;
      background: yellow;
      padding: 5px;
      margin: 10px;
    }

    .conteiner2 .item1 {
      background: green;
    }
    .conteiner2 .item2 {
      background: green;
      width: 460px;
    }

    .conteinerBlue {
      width: 300px;
      height: 300px;
      background: blue;
      display: flex;
      flex-flow: row wrap;
      justify-content: stretch;
    }

    .conteinerBlue .conteinerYellow {
      position: absolute;
      width: 150px;
      height: 150px;
      margin: 75px;
      background: yellow;
    }

    .conteinerYellow .conteinerRed{
      position: absolute;
      width: 50px;
      height: 50px;
      margin: 50px;
      background: red;
    }

    .conteiner4 {
      display: flex;
      flex-flow: row wrap;
      width: 200px;
    }

    .conteiner4 .item{
      width: 30px;
      height: 30px;
      background: blue;
      padding: 5px;
      margin: 10px;
      flex-direction: row;
      text-align: left;
    }

    .conteiner4 .item1{
      width: 30px;
      height: 70px;
      background: blue;
      padding: 5px;
      margin: 10px;
      flex-direction: row;
      text-align: left;
    }
  </style>
  
