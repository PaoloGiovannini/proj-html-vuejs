<script>
import PageHeader from './components/PageHeader.vue';
import PageMain from './components/PageMain.vue';
import PageFooter from './components/PageFooter.vue';
export default{
  components:{
    PageHeader,
    PageMain,
    PageFooter
  },
  data(){
    return{
      navbar: ['HOME', 'SERVICES', 'ABOUT', 'PROJECTS', 'RESULTS', ],
      voiceMenu: [
                {
                  titolo: 'About',
                  voci: ['The Company', 'Institutional', 'Social & Events', 'Innovation', 'Enviroment', 'Technology']
                    
                },
                {
                  titolo: 'Services',
                  voci: ['Audit & Assurance', 'Financial Advisory', 'Analytics M&A', 'Middle Marketing', 'Legal Consulting', 'Regulatory Risk' ]
                    
                },
                {
                  titolo: 'Support',
                  voci: ['Responsability', 'Terms of Use', 'About Cookies', 'Privacy Policy', 'Accessibility', 'Information']
                    
                },
            ]
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
  <footer>
    <PageFooter
    :voices="this.voiceMenu"/>
  </footer>

</template>

<style lang="scss">
@use './styles/general.scss';

</style>
