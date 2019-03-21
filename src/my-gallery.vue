<template lang="html">
  <div class="wrapper">
    <div class="card" v-for="(item, id) in cards">
      <!-- <img class="image" :src="item.img" alt="asd"> -->
      <div class="image " :style='{ backgroundImage: `url(${item.img})`}'></div>
      <div class="text">{{item.text}}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      color: '#2cc3f9',
      cards:[
        {img: 'image/mauntain.jpg', text: 'eram tamen eram summis quae fore quis velit sint quis dolore labore labore multos multos veniam nisi quem esse culpa'},
        {img: 'image/altitude-clouds-cold-417173.jpg', text: 'dolore minim eram quid tamen export labore dolore legam sint dolore ipsum anim labore aute'},
        {img: 'image/adventure-alpine-altitude-355241.jpg', text: 'malis tamen elit eram esse quid labore quem irure veniam eram minim aute quae nulla ipsum minim'},
        {img: 'image/altitude-clouds-cold-417173.jpg', text: 'ipsum irure aute quae legam ipsum noster dolor enim summis quorum esse nulla minim eram enim tamen dolor sint eram fugiat fore export quorum dolor irure quid enim quae quorum'},
        {img: 'image/android-wallpaper-cold-daylight-1366919.jpg', text: 'quid quae velit malis elit dolor nulla minim enim summis'},
        {img: 'image/android-wallpaper-dawn-daylight-1366909.jpg', text: 'fore fore nisi ipsum sunt nisi quae dolore noster amet quem irure quorum culpa velit'},
        {img: 'image/astronomy-constellations-hd-wallpaper-1624504.jpg', text: 'dolore sint aliqua amet aute sint malis quae amet labore magna duis minim dolor quid aliqua veniam nulla'},
      ]
    }
  }
}
</script>

<style lang="css" scoped>
  .wrapper{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 1fr);
    grid-gap: 5vh;
    width: 80%;
    margin: 20px auto 20px 10%;
  }
  .card{
    box-shadow: 5px 5px 5px rgba(0,0,0,0.5);
  }
  .image{
    position: relative;
    width: 100%;
    height: 30vh;
    background: #da85aa;
    background-size: cover;
    background-position: center;
    transition: opacity, transform .5s;
  }
  .card:hover .image{
    transform: translateY(2px);
    opacity: .8;
  }
  .text{
    display: grid;
    font-family: cursive;
    height: 18vh;
    width: 90%;
    margin-left: 5%;
    align-items: center;
  }
</style>
