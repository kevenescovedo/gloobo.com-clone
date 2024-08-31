<template>

    <div class="new-grid">
        <newsComponentVue 
        v-for="(noticia, index) in noticias"
         :key="index"
         :foto="noticia.foto_capa" :titulo="noticia.titulo_capa"
         :chamada="noticia.chamada_capa" :link="noticia.link_noticia"
        />
    </div>
</template>

<script>
import newsComponentVue from '../news_component/newsComponent.vue';

export default {
    name: "NewsGridComponent",
    data() {
      return {
        noticias:[
            {
                titulo_capa: "Inflação oficial sobe para 0,38% em julho, puxada pela gasolina",
                //chamada_capa : "Em 12 meses, IPCA de 4,5% está no limite da meta do governo",
                foto_capa: "https://cbnprudente.com.br/_upload/foto/noticia/09-08-202403-11-28fundodetexturadedinheirobrasileironotasbrasileirasde50reaisenotasbrasileirasde100rea.png",
                link_noticia: "https://cbnprudente.com.br/regiao/1580/inflacao-oficial-sobe-para-038-em-julho-puxada-pela-gasolina",
            },

          

            {
                titulo_capa: "Papo de Vinho: Uma saborosa união entre os alimentos embutidos e o vinho",
                //chamada_capa: "Os portugueses trouxeram a charcutaria para o Brasil.",
                foto_capa: "https://cbnprudente.com.br/_upload/foto/noticia/09-08-202411-37-24CHARCUTARIA.jpeg",
                link_noticia: "https://cbnprudente.com.br/presidente-prudente/1577/papo-de-vinho-uma-saborosa-uniao-entre-os-alimentos-embutidos-e-o-vinho",
            },

            {
                titulo_capa: "Dois colégios rurais batem nível inédito em Matemática",
               // chamada_capa: "69% dos estaduais obtém menores níveis no Ideb",
                foto_capa: "https://s2-home-globo.glbimg.com/ZQIsTUKyx_jzMYuoJsnFVT31yWQ=/355x353:804x606/fit-in/629x354/middle/smart/filters:strip_icc():strip_exif()/i.s3.glbimg.com/v1/AUTH_da025474c0c44edd99332dddb09cabe8/internal_photos/bs/2024/J/B/DRSDM2RuauZa9OUK2xqA/melhor-escola-publica-do-brasil.jpeg",
                link_noticia: "https://oglobo.globo.com/brasil/educacao/noticia/2024/08/17/duas-escolas-estaduais-atingem-niveis-ineditos-de-ensino-em-matematica-veja-a-lista-das-cem-com-maior-aprendizagem.ghtml",
            },

            {
                titulo_capa: "As principais frases dos candidatos de SP ditas ao g1",
                //chamada_capa: "Destaques das entrevistas dos candidatos no Rio",
                foto_capa: "https://s2-home-globo.glbimg.com/AU5vo_U9uZwS7NHr9s1PILH0Nm8=/4x16:1893x1080/fit-in/629x354/middle/smart/filters:strip_icc():strip_exif()/i.s3.glbimg.com/v1/AUTH_59edd422c0c84a879bd37670ae4f538a/internal_photos/bs/2024/U/r/4NPx0SRXKCdIsazvkmAg/montagem-tabata-amaral-jose-luiz-datena-guilherme-boulos-pablo-marcal-ricardo-nunes.jpg",
                link_noticia: "https://g1.globo.com/sp/sao-paulo/eleicoes/2024/noticia/2024/08/17/veja-as-principais-frases-ditas-por-candidatos-a-prefeitura-de-sp-em-entrevista-ao-g1.ghtml",
            },

            {
                titulo_capa: "Após calorão, onda de frio derruba temperaturas e traz chuva ao interior de SP a partir deste sábado",
                //chamada_capa: "Veja Temperatura na sua região",
                foto_capa: "https://s2-g1.glbimg.com/iT5wlHMfqgf5BCNSMTud_ETNTh8=/540x304/top/smart/https://i.s3.glbimg.com/v1/AUTH_59edd422c0c84a879bd37670ae4f538a/internal_photos/bs/2023/t/K/qAMiLbRgaBf7z680Zreg/chuvas-de-verao-defesa-civil-auditorio-57.jpg",
                link_noticia: "https://g1.globo.com/sp/sorocaba-jundiai/noticia/2024/08/23/apos-calorao-onda-de-frio-derruba-temperaturas-e-traz-chuva-ao-interior-de-sp-a-partir-deste-sabado.ghtml",

            },

            {
                titulo_capa: "O que acontece agora que vitória de Maduro foi validada",
                //chamada_capa: "Veja o quje disse a oposição",
                foto_capa: "https://s2-home-globo.glbimg.com/wxdv0XaKGP2o0ztG-0oCULIiReo=/74x14:1024x548/fit-in/515x290/middle/smart/filters:strip_icc():strip_exif()/i.s3.glbimg.com/v1/AUTH_59edd422c0c84a879bd37670ae4f538a/internal_photos/bs/2024/u/X/eBBSYWQf22GFztEToQAQ/000-36dc7ep.jpg",
                link_noticia: "https://g1.globo.com/mundo/noticia/2024/08/24/crise-na-venezuela-3-possiveis-cenarios-para-futuro-do-pais-apos-supremo-chancelar-vitoria-de-maduro.ghtml",

            }


        ]
      }
    },
    components: {
    newsComponentVue
    },
    methods: {

    }
}
</script>

<style>
 .new-grid {
    width:  65%;
    max-width: 900px;
    height: 600px;
    /*background-color: brown;*/
    margin: 20px auto;
    display: flex;
    flex-direction: row;
    justify-content: start;
    height: auto;
    flex-wrap: wrap;
  }
  @media (max-width: 1500px) {
    .new-grid {
        justify-content: center;
     }
}

@media (max-width: 1000px) {
    .new-grid {
        flex-direction: column;
     }
}
</style>
