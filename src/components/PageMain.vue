<script>
import SectionBusiness from './MiscellaneousComponents/SectionBusiness.vue';
import SectionCompany from './MiscellaneousComponents/SectionCompany.vue';
import SectionProjects from './MiscellaneousComponents/SectionProjects.vue';
import SectionResults from './MiscellaneousComponents/SectionResults.vue';
export default{
    name: 'PageMain',
    components:{
        SectionBusiness,
        SectionCompany,
        SectionProjects,
        SectionResults,

    },
    data(){
        return{
            actionsAndProjects: ['ALL', 'INSTITUTIONAL', 'SOCIAL', 'EVENTS', 'INNOVATION', 'ENVIROMENT', 'TECHNOLOGY']
        }
    }

}
</script>

<template>

<SectionBusiness/>
<SectionCompany/>
<SectionProjects
    :actions ="this.actionsAndProjects"/>
<SectionResults/>
</template>

<style scoped lang="scss">


</style>
