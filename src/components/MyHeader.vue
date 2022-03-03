<template>
    <div>
        <MyNav/>
        <MyJumbotron/>
    </div>
</template>

<script>
import MyNav from './partials/Header/MyNav.vue'
import MyJumbotron from './partials/Header/MyJumbotron.vue'

export default {
    name: 'MyHeader',
    components: {
        MyNav,
        MyJumbotron
    }
    
}
</script>

<style lang="scss" scoped>

</style>