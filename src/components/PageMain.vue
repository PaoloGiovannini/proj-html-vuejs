<script>
import SectionBusiness from './MiscellaneousComponents/SectionBusiness.vue';
import SectionCompany from './MiscellaneousComponents/SectionCompany.vue';
export default{
    name: 'PageMain',
    components:{
        SectionBusiness,
        SectionCompany
    }

}
</script>

<template>

<SectionBusiness/>
<SectionCompany/>
</template>

<style scoped lang="scss">


</style>
