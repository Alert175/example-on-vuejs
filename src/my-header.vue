<template lang="html">
  <div class="wrapper-nav">
      <div class="navigation">
        <a href="#" v-for="item in items">{{item}}</a>
      </div>
      <div class="wrapper-text">
        <h1>Hello dear friend!</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            items: [
                'Главная',
                'О нас',
                'Отзывы'
            ]
        }
    }
}
</script>

<style lang="css" scoped>
    .wrapper-nav{
      background-image: url("./assets/contant.jpg");
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center;
      height: 100vh;
    }
    .navigation{
      display: grid;
      justify-items: center;
      align-items: center;
      grid-template-columns: repeat(3, 1fr);
      grid-template-rows: 10vh;
    }
    .navigation a{
      font-family: sans-serif;
      font-size: 30px;
      color: #d8dee2;
      text-decoration: none;
      border-bottom: 1.5px solid #010916;
      transition: border-color .5s;
    }
    .navigation a:hover{
      border-color: #d8dee2;
    }
    .wrapper-text{
      display: grid;
      grid-template-rows: 1fr 1fr;
      grid-row-gap: 5vh;
      grid-template-areas:
        "h1"
        "p";
      justify-items: center;
    }
    .wrapper-text h1{
      grid-area: h1;
      align-self: center;
      text-align: center;
      font-family: fantasy;
      font-size: 60px;
      width: 80%;
      color: #e9f5f5;
    }
    .wrapper-text p{
      grid-area: p;
      width: 80%;
      font-family: cursive;
      font-size: 25px;
      color: #e9f5f5;
      vertical-align: bottom;
    }
</style>
