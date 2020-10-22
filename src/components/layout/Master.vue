<template>
    <div class="wrapper">
        <!-- Loader -->
        <transition name="fade">
            <div class="loader-container" v-show="show">
                <div class="loader"></div>
            </div>
        </transition>
        <slot name="header"></slot>
        <slot name="main"></slot>
        <slot name="footer"></slot>
    </div>
</template>
<style lang="scss" src="@/assets/sass/styles.scss">

</style>
<style lang="scss" src="@/assets/sass/responsive.scss">

</style>
<script>
export default{
    props:['show']
}
</script>