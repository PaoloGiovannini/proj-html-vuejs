<script>

export default{
    name: 'ButtonTouch',
}
</script>

<template>

    <div class="button">
        <span>GET IN TOUCH</span>
    </div>



</template>

<style scoped lang="scss">
@use '../../styles/partials/variables';
@use '../../styles/partials/mixins';

.button{
   
    @include mixins.button;
}

</style>
