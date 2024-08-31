<template>
   <MenuComponent  @open-menu="changeMenu"/>
  <SideBarComponent :classSidebar="classSidebar" :classFundo="fundoClass"  @close-menu="changeMenu"/>
 <HomePage/>
</template>

<script>
import HomePage from './pages/home/HomePage.vue'
import MenuComponent  from './components/menu/MenuComponent.vue';
import SideBarComponent from './components/sidebar/SideBarComponent.vue';

export default {
  name: 'App',
  components: {
   MenuComponent,
   SideBarComponent,
   HomePage,
  },
  data() {
    return {
      classSidebar: 'sidebar-close',
      fundoClass: 'fundo-close',
      isOpenMenu: false// Inicialmente sem estilo
    }
  },
  methods: {
    changeMenu() {
      console.log("aaaaaaaaaaaaaaaaaaa");
      if(this.isOpenMenu == false) {
        this.isOpenMenu = true;
        this.classSidebar = 'sidebar-open';
        this.fundoClass = 'fundo-open';

        document.body.style.overflow = "hidden";
        document.body.style.height = "100vh";
        // Para evitar problemas com o layout
        
             
      } else {
        
        this.isOpenMenu = false;
        this.classSidebar = 'sidebar-close';
        this.fundoClass = 'fundo-close';
        document.body.style.overflow = "scroll";
        document.body.style.height = "100%";

       
        }
      }
     // Atualiza o objeto de estilo
    }
  }

</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #fafafa;
  /*margin-top: 60px;*/
}

</style>
