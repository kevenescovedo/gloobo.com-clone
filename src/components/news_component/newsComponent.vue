<template>
  <div class="new-component">
     <img :src="foto" alt="foto" class="foto-news"/>
     <h3 class="titulo-news">{{titulo }}</h3>

     <h4>{{ chamada }}</h4>
    </div></template>

<script>
export default {
    name: "NewsComponent",
    methods: {

    },
    props: {
    titulo: String,
    chamada: String,
    foto: String,
    link: String
  }
}
</script>

<style>
 .new-component {
    display: flex;
    flex-direction: column;
    padding: 20px 10px;
    width: 30%;
    border: 1px solid transparent;
    background-color: white;
    margin: 15px;
    min-height: 250px;
    max-height: 300px;
    border-radius: 20px;
    cursor: pointer;

   
  }
  .link-news {
    all: unset;
    display: block;
    text-decoration: none;
    cursor: pointer;
   
  }
  .foto-news {
    width: 100%;
    height: 60%;
    margin: 10px 0;

    border-radius: 20px;


  }
  .titulo-news {
    font-size: 20px;
    font-weight: bold;
    /*text-align: start;*/
    color: #2f54e8;
    margin-bottom: 20px;
  }
  h4 {
    text-align: start;
    color: gray;
  }

  @media (max-width: 1000px) {
    .new-component {
      width: 100%;
     height: auto;
     max-height: unset;
      margin: 20px 0;
    }
    .titulo-news {
      font-size: 1em;

    }
}


</style>
