<script>
import SectionBusiness from './MiscellaneousComponents/SectionBusiness.vue';
import SectionCompany from './MiscellaneousComponents/SectionCompany.vue';
import SectionProjects from './MiscellaneousComponents/SectionProjects.vue';
import SectionResults from './MiscellaneousComponents/SectionResults.vue';
import SectionForm from './MiscellaneousComponents/SectionForm.vue';
export default{
    name: 'PageMain',
    components:{
        SectionBusiness,
        SectionCompany,
        SectionProjects,
        SectionResults,
        SectionForm,

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
<SectionForm/>
</template>

<style scoped lang="scss">


</style>
