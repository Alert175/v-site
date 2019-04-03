<template lang="html">
  <div class="wrapper">
    <div class="wrapper-gallery">
      <div class="wrapper-cards" v-for="(item, id) in cards">
        <div class="image" :style='{ backgroundImage: `url(${item.img})`}'></div>
        <div class="text">{{item.text}}</div>
      </div>
    </div>
    <div class="inputInfo">
      <input type="text" v-model="cardImage" placeholder="Укажите адрес фото">
      <input type="text" v-model="cardText" placeholder="Укажите подпись">
      <button type="button" name="button" @click="addCard">Добавить карточку</button>
    </div>
  </div>

</template>

<script>
export default {
  data(){
    return{
      cardImage: '',
      cardText: '',
      cards:[
        {img: 'image-gallery/girl.jpg', text: 'eram tamen eram summis'},
        {img: 'image-gallery/-185517.jpg', text: 'multos esse export export illum tempor minim'}
      ]
    }
  },
  methods:{
    addCard: function() {
      if (this.cardImage == '' || this.cardText == '') {
        alert('Заполните поля.')
      } else {
        this.cards.push({img: this.cardImage, text: this.cardText});
        this.cardImage = '';
        this.cardText = '';
      }
    }
  }
}
</script>

<style lang="css" scoped>
  .wrapper{
    display: grid;
    background: #f7edd2;
  }
  .wrapper-gallery{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 1fr;
    grid-gap: 20px;
    min-height: 78vh;
    margin: 1vh auto;
  }
  .wrapper-cards{
    display: grid;
    height: 40vh;
    width: 80%;
    justify-self: center;
    background: #f7e4df;
    -webkit-box-shadow: 5px 5px 10px #222222;
            box-shadow: 5px 5px 10px #222222;
    -webkit-transition: .5s;
    transition: .5s;
  }
  .wrapper-cards:hover{
    opacity: .95;
    -webkit-transform: translate3d(-10px, 0px, 10px);
            transform: translate3d(-10px, 0px, 10px);
    -webkit-box-shadow: 10px 10px 20px #222222;
            box-shadow: 10px 10px 20px #222222;
  }
  .wrapper-cards .image{
    height: 30vh;
    background: #7834a1;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
  }
  .wrapper-cards .text{
    height: 10vh;
    text-align: center;
    font-family: 'Indie Flower', 'Neucha', cursive;
    font-size: 25px;
  }
  .wrapper .inputInfo{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 10vh;
    grid-gap: 20px;
    background: #211c00;
  }
  .wrapper .inputInfo input, button{
    justify-self: center;
    -ms-flex-item-align: center;
        align-self: center;
    width: 50%;
    height: 8vh;
    text-align: center;
    border: none;
    background: #f7edd2;
    font-family: 'Montserrat Alternates', sans-serif;
    font-size: 15px;
  }
</style>
