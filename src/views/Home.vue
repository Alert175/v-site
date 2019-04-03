<template lang="html">
  <div class="wrapper">
    <div class="section-home">
      <h1>Nature</h1>
    </div>
    <div class="section-text">
        <div class="text">
          <h1>Beauty</h1>
          <p>Deserunt e dolor aliquip de nostrud culpa incurreret admodum.

              Proident te summis, est tempor singulis comprehenderit.

              Amet aliquip ut laboris, se esse officia efflorescere.

              Litteris et fabulas do labore nostrud qui imitarentur.

              Esse cernantur an efflorescere est litteris legam esse officia malis.</p>
          <p>Quo commodo id quibusdam sed deserunt an quis appellat.

              Deserunt eu eram, e vidisse ex eiusmod.</p>
        </div>
        <div class="wrap-photo">
          <div class="photo"></div>
        </div>
    </div>
  </div>
</template>

<style lang="css" scoped>
  .section-home{
    display: grid;
    min-height: 90vh;
    width: 100%;
    -webkit-box-align: center;
        -ms-flex-align: center;
            align-items: center;
    -webkit-box-pack: center;
        -ms-flex-pack: center;
            justify-content: center;
    background: url('../assets/beautiful-beauty-colors-2040406.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    -webkit-perspective: 500px;
            perspective: 500px;
  }
  .section-home h1{
    font-family: 'Raleway', sans-serif;
    font-size: 55px;
    color: #ab672f;
    padding: 10px 20px;
    border: 1px solid #ab672f;
    -webkit-transform-style: inherit;
            transform-style: inherit;
    -ms-flex-item-align: center;
        align-self: center;
    -webkit-transition: .5s;
    transition: .5s;
  }
  .section-home h1:hover{
    -webkit-transform: rotate3d(1, 1, 1, 30deg);
            transform: rotate3d(1, 1, 1, 30deg);
    background: #f7f7c6;
  }
  .section-text{
    display: grid;
    min-height: 100vh;
    width: 90%;
    margin-left: 5%;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 80vh;
    grid-column-gap: 20px;
    -ms-flex-line-pack: distribute;
        align-content: space-around;
  }
  .section-text h1, p{
    text-align: center;
  }
  .section-text h1{
    font-family: 'Raleway', sans-serif;
    font-size: 55px;
  }
  .section-text p{
    font-family: 'Nanum Gothic', sans-serif;
    font-size: 25px;
  }
  .section-text .wrap-photo{
    -webkit-perspective: 500px;
            perspective: 500px;
  }
  .section-text .photo{
    width: 100%;
    height: 100%;
    background-image: url('../assets/girl.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    -webkit-box-shadow: 5px 5px 10px #222222;
            box-shadow: 5px 5px 10px #222222;
    -webkit-transition: .5s;
    transition: .5s;
  }
  .section-text .photo:hover{
    opacity: .95;
    -webkit-transform: translate3d(-10px, 0px, 10px);
            transform: translate3d(-10px, 0px, 10px);
    -webkit-box-shadow: 10px 10px 20px #222222;
            box-shadow: 10px 10px 20px #222222;
  }
  @media screen and (max-width: 900px) {
    .section-text{
      grid-template-columns: 1fr;
      grid-template-rows: 1fr 1fr;
    }
  }
</style>
