<template lang="html">
  <div class="wrapper-blog">
    <div class="blog-card hover" v-for="post in blogPosts">
      <div class="headPost">
        <p>{{post.headline}}</p>
      </div>
      <div class="textPost">
        <p>{{post.text}}</p>
      </div>
    </div>
    <div class="templatePost blog-card hover">
      <input type="text" v-model="postHead" placeholder="Заголовок поста">
      <textarea type="text" v-model="textPost" placeholder="Описание поста"></textarea>
      <button type="button" @click="addPost">Добавить пост</button>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      postHead: '',
      textPost: '',
      blogPosts: [
        {headline: 'irure noster anim', text: 'summis fugiat sunt quae fore sint legam amet ipsum quorum labore magna fugiat nulla cillum minim fore magna culpa esse fore irure duis tamen noster'},
        {headline: 'labore', text: 'illum veniam summis malis fugiat esse labore multos veniam aliqua legam dolor veniam cillum quem legam ipsum aliqua veniam amet illum fugiat quorum quis malis legam quorum tempor legam sunt sint fugiat fugiat illum eram fugiat anim culpa noster export sunt quorum magna sunt irure quid quem veniam anim malis'}
      ]
    }
  },
  methods:{
    addPost: function() {
      if (this.postHead == '' || this.textPost == '') {
        alert('Заполните все поля')
      }
      else {
        this.blogPosts.push({headline: this.postHead, text: this.textPost});
        this.postHead = '',
        this.textPost = ''
      }
    }
  }
}
</script>

<style lang="css" scoped>
  .wrapper-blog{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 40vh;
    grid-gap: 20px;
    margin: 10px 10px;
    -webkit-box-align: center;
        -ms-flex-align: center;
            align-items: center;
  }
  .blog-card{
    display: grid;
    width: 80%;
    justify-self: center;
    background: #f6f6f6;
    -webkit-box-shadow: 5px 5px 10px #222222;
            box-shadow: 5px 5px 10px #222222;
    -webkit-transition: .5s;
    transition: .5s;
  }
  .blog-card .headPost{
    display: grid;
    height: 10vh;
    width: 90%;
    margin-left: 5%;
    text-align: center;
    -webkit-box-align: center;
        -ms-flex-align: center;
            align-items: center;
    font-family: 'Anton', sans-serif;
    font-size: 25px;
  }
  .blog-card .textPost{
    display: grid;
    height: 30vh;
    width: 90%;
    margin-left: 5%;
    text-align: center;
    -webkit-box-align: center;
        -ms-flex-align: center;
            align-items: center;
    font-family: 'Libre Baskerville', serif;
  }
  p{
    margin: 0;
  }
  .templatePost{
    display: grid;
    grid-template-rows: 10vh 20vh 10vh;
    -webkit-transition: .5s;
    transition: .5s;
  }
  .templatePost input, textarea, button{
    text-align: center;
    border: none;
    font-family: 'Montserrat Alternates', sans-serif;
    font-size: 20px;
    width: auto;
  }
  .hover:hover{
    -webkit-transform: translate3d(-10px, 10px, 0px);
            transform: translate3d(-10px, 10px, 0px);
  }
  @media screen and (max-width: 1100px){
    .blog-card .textPost{
      font-size: 15px;
    }
    .templatePost input, textarea, button{
      width: 100%;
    }
    textarea{
      width: auto;
    }
  }
  @media screen and (max-width: 1100px){
    .wrapper-blog{
      grid-template-columns: 1fr 1fr;
      grid-template-rows: auto;
    }
  }
  @media screen and (max-width: 620px){
      .wrapper-blog{
        grid-template-columns: 1fr;
        grid-template-rows: auto;
      }
    }
</style>
