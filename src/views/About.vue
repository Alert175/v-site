<template lang="html">
  <div class="wrapper">
    <div class="wrapper-contact">
      <div class="info">
        <p>Вы можете найти нас по адресу:</p>
        <p>город Краснодар улица Калинина 20</p>
        <p>Телефон для связи: <br>8 (800) 555 35 35</p>
      </div>
      <div class="map">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d10044.338826727673!2d38.92442797084428!3d45.05339983253774!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x40f04f3ea98d38eb%3A0xa68e1766b1cdd5d0!2z0JHQvtGC0LDQvdC40YfQtdGB0LrQuNC5INGB0LDQtCDQuNC8LiDQmC7QoS4g0JrQvtGB0LXQvdC60L4gKNCU0LXQvdC00YDQsNGA0LjQuSk!5e0!3m2!1sru!2sru!4v1554314551493!5m2!1sru!2sru" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
      </div>
    </div>
    <div class="footer">
      <p>Это тестовый проект для портфолио</p>
    </div>
  </div>

</template>

<script>
export default {
}
</script>

<style lang="css" scoped>
  .wrapper-contact{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 80vh;
    grid-row-gap: 20px;
    -webkit-box-align: center;
        -ms-flex-align: center;
            align-items: center;
  }
  .wrapper-contact .info p{
    margin: 10% 20%;
    font-family: 'Exo 2', sans-serif;
    font-size: 35px;
    -webkit-transition: .5s;
    transition: .5s;
  }
  .wrapper-contact .info p:hover{
    -webkit-transform: translate3d(-10px, 0px, 10px);
            transform: translate3d(-10px, 0px, 10px);
    -webkit-transform: scale(1.2);
            transform: scale(1.2);
  }
  .wrapper-contact iframe{
    -webkit-box-shadow: 5px 5px 10px #222222;
            box-shadow: 5px 5px 10px #222222;
    -webkit-transition: .5s;
  }
  .wrapper .footer{
    display: grid;
    height: 10vh;
    text-align: center;
    background: #1f2825;
    color: #cce5f9;
    font-family: 'Exo 2', sans-serif;
    font-size: 25px;
    -webkit-box-align: center;
        -ms-flex-align: center;
            align-items: center;
  }
  .wrapper .footer p{
    margin: 0;
  }
</style>
