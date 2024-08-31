<template>
   <div id="fundo-sidebar" @click="closeMenu"  :class=classFundo>
    
    <div id="sidebar" @click.stop  :class=classSidebar>
        <img @click="closeMenu" id="closeMenu" style="margin-top:10px; margin-bottom: 10px;" src="../../assets/icons/icons8-back-48.png" height="30" width="30"/>
        <nav>
           <LinkSideBarComponentVue title="G1" link="https://g1.globo.com/" icon="https://s3.glbimg.com/v1/AUTH_fd78dc4be9404a2e92b908ade306e9e6/prod/header_menu_svgs/g1.svg" />
           <LinkSideBarComponentVue title="O Globo" link="https://oglobo.globo.com/" icon="https://s3.glbimg.com/v1/AUTH_fd78dc4be9404a2e92b908ade306e9e6/prod/header_menu_svgs/oglobo.svg" />
           <LinkSideBarComponentVue title="Valor" link="https://valor.globo.com/?utm_source=globo.com&utm_medium=menuburguer" icon="https://s3.glbimg.com/v1/AUTH_fd78dc4be9404a2e92b908ade306e9e6/prod/header_menu_svgs/valor.svg" />
           <LinkSideBarComponentVue title="GE" link="https://ge.globo.com/?utm_source=globo.com&utm_medium=menuburger" icon="https://s3.glbimg.com/v1/AUTH_fd78dc4be9404a2e92b908ade306e9e6/prod/header_menu_svgs/ge.svg" />
           <LinkSideBarComponentVue title="Cartola" link="https://ge.globo.com/cartola/?utm_source=globocom&utm_medium=menuburguer&utm_campaign=c2022_10_cartola_cartola-2022_alcance&utm_content=MEN_cartola-2022" icon="https://s3.glbimg.com/v1/AUTH_fd78dc4be9404a2e92b908ade306e9e6/prod/header_menu_svgs/cartolafc.svg"/>
           <LinkSideBarComponentVue title="GloboPlay" link="https://globoplay.globo.com/?origemId=1760&utm_source=gcom&utm_medium=home&utm_campaign=gcom-botao-destaque-superior" icon="https://s3.glbimg.com/v1/AUTH_fd78dc4be9404a2e92b908ade306e9e6/prod/header_menu_svgs/globoplay.svg"/>
           <LinkSideBarInterno title="Notícias" link=""/>
           <LinkSideBarInterno title="Comentaristas" link=""/>
           <LinkSideBarInterno title="Assinaturas" link=""/>
           <LinkSideBarInterno title="Previsão do Tempo" link=""/>
           <LinkSideBarInterno title="Premiere" link=""/>
           <LinkSideBarInterno title="Podcast" link=""/>
           
        </nav>
    </div>
</div>
  
</template>

<script>
import LinkSideBarComponentVue from '../link_sidebar/LinkSideBarComponent.vue';
import  LinkSideBarInterno from '../link_sidebar/LinkSideBarInterno.vue';

export default {
    name: "SideBarComponent",
    components: {
        LinkSideBarComponentVue,
        LinkSideBarInterno,
    },
    props: {
    classSidebar: {
      type: String,
      default: () => ('')
    },
    classFundo: {
      type: String,
      default: () => ('')
    }
  },
  methods: {
    closeMenu() {
        console.log('btrgtrg');
        this.$emit('close-menu'); 
    }
  }
}
</script>
<style>
#fundo-sidebar {
    
    position: fixed;
   
    background-color: rgba(0,0,0,0.5);
    height: 100%;
    width: 100%;
 
  

}

#sidebar {
    height: 100vh; /* 100% da altura da viewport */
    position: fixed;
  overflow-y: auto;
    display: flex;
    flex-direction: column;
    align-items: start;
    background-color: #fff;
    width: 20%;
    height: 100%;
   
   
}

.sidebar-close {
  left: -100%;
  transition: all 2s ease;
}
.sidebar-open {
  left: 0 !important;
  transition: all 0.5s ease;

}
.fundo-open {
 width: 100%;
 visibility: visible;

}
.fundo-close {
  width: 0%;
 visibility: hidden;
 transition-delay: 1s;
}
.sidebar img {
    cursor: pointer;
}

#closeMenu {
  cursor: pointer;
}

@media (max-width: 800px) {
    #sidebar {
        width: 70%;
  }
}
</style>