<script>

export default{
    name: 'ButtonTouch',
}
</script>

<template>

    <div class="button">
        <a href="#info-company">GET IN TOUCH</a>
    </div>



</template>

<style scoped lang="scss">
@use '../../styles/partials/variables';
@use '../../styles/partials/mixins';

.button{
   
    @include mixins.button;
    a{
        text-decoration: none;
        color: white;
    }
}

</style>
