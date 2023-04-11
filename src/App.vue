<script>
import PageHeader from './components/PageHeader.vue';
import PageMain from './components/PageMain.vue';
export default{
  components:{
    PageHeader,
    PageMain
  },
  data(){
    return{
      navbar: ['HOME', 'SERVICES', 'ABOUT', 'PROJECTS', 'RESULTS', ]
    }
  }
}
</script>

<template>
  <header>
    <PageHeader
      :navbar="this.navbar"/>
  </header>
  <main>
    <PageMain/>
  </main>

</template>

<style lang="scss">
@use './styles/general.scss';

</style>
