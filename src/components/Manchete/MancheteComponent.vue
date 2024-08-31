<template>
       <div class="component">
        <div class="container">
        <div class="manchete">
            <span class="chapeu">Promessas dos políticos</span>
            <h1 class="titulo-manchete">Prefeitos cumpriram menos da metade das promessas de segurança, saúde e educação</h1>
            <div style="height: 40px;"></div>
        </div>

        <div class="destaques" style="margin-top: 20px;">
                    <div class="noticia" style="background-image: url('https://nsc-total-wp.s3.sa-east-1.amazonaws.com/wp-content/uploads/legacy/s3fs-public/graphql-upload-files/atletas%20do%20volei%20masculino%20olimpiadas_0.jpg');">
                            <div class="fundo">
                                <span class="chapeu" style="color: white;">Voleibol</span>
                                <h1 class="titulo-card">No Voleibol Brasil vence o Egito e se classifica</h1>
                                
                            </div>
                    </div>
            <div class="noticia" style="background-image: url('https://www.guarulhoshoje.com.br/wp-content/uploads/2024/07/assasa.jpg');">
                 <div class="fundo">
                    <span class="chapeu" style="color: white;">Olimpiadas 2024</span>
                        <h1 class="titulo-card">Veja como está o brasil no ranking nas olimpiadas de Paris</h1>
                 </div>
            </div>
        </div>
    </div>
       </div>
</template>

<script>
export default {
    name: "MancheteComponent",
   
}

</script>
<style>
* {
    box-sizing: border-box;
}
.component {
    width: 100%;
}
 .container {
    width: 80%;
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;align-items: center;
   
 }
.manchete {
    border: 1px solid #c2bcbc;
    width: 40%;
    height: 520px;
    border-radius: 20px;
    background-color: white;
}
.destaques {
    width: 40%;
}
.noticia {
    margin:0 20px;
    margin-bottom: 20px;
    border-radius: 20px;
   
    height: 250px;
    background-color : #f1f1f1;
}
.chapeu {
    font-weight: bold;
    font-size: 14px;
    text-align: start;
}

/* content macnhete */
.manchete {
    padding: 20px;
    display: flex;
    flex-direction: column;
    cursor: pointer;
    justify-content: space-between;
    align-items: start;
}

.titulo-manchete {
    text-align: start;
    
}

.noticia { 
background-size: cover;
background-position: center;
 transition: all .5s;


}
.noticia .fundo {
    height: 100%;
    width: 100%;
    cursor: pointer;
    background: radial-gradient(circle, transparent, rgba(0, 0, 0, 0.95));
    border-radius: 20px;
  
    z-index: 1;
}
/*.chapeu.noticia:hover {
    transform: scale(1.2);
}*/

.titulo-card {
    text-align: start;
    color: white;
    font-size: 25px;
    
}
.fundo {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-content: start;
    padding: 20px;

}
@media only screen and (max-width: 1000px) {
 .container {
    flex-direction: column;
    margin-top: 20px;
 }
 .manchete {
    width: 60%;
 }
 .destaques {
   
    width: 60%;
 }
 .noticia {
    margin-left: 0;
    margin-right: 0;
 }
}
 @media only screen and (max-width: 1000px) {
  .manchete {
     width: 80%;
  }
  .destaques {
     width: 80%;
  }
}


@media only screen and (max-width: 600px) {
  .manchete {
     width: 90%;
  }
  .destaques {
     width: 90%;
  }
}


@media only screen and (max-width: 400px) {
  .manchete {
     width: 100%;
  }
  .destaques {
     width: 100%;
  }
}



</style>