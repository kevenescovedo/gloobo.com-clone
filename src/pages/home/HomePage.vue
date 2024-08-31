
<template>
<div id="home-page">
    <MancheteComponent/>
    <NewsGridComponentVue/>
</div>
   
</template>

<script>
import NewsGridComponentVue from '@/components/news_grid/newsGridComponent.vue';
import MancheteComponent from '../../components/Manchete/MancheteComponent.vue';




export default{
   name: 'HomePage', 
   components: {
    MancheteComponent,
    NewsGridComponentVue
    
   }
 
};
</script>
<style scoped>
#home-page {
    padding-top: 80px;
    height: 100%;
    width: 100%;
}
</style>