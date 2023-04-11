<script>
import PageHeader from './components/PageHeader.vue';
export default{
  components:{
    PageHeader
  },
  data(){
    return{
      navbar: ['HOME', 'SERVICES', 'ABOUT', 'PROJECTS', 'RESULTS', ]
    }
  }
}
</script>

<template>
<PageHeader
  :navbar="this.navbar"/>
</template>

<style lang="scss">
@use './styles/general.scss';

</style>
