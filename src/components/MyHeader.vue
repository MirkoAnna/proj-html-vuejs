<template>
    <div>
        <MyNav :links="links"/>
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
    },
    data() {
        return {
            links: [
                {
                    text: 'Home',
                    url: '#'                    
                },
                {
                    text: 'About',
                    url: '#About'
                },
                {
                    text: 'Academics',
                    url: '#'
                },
                {
                    text: 'Courses',
                    url: '#'
                },
                {
                    text: 'News',
                    url: '#'
                }
            ],
        }
    }
}
</script>

<style lang="scss" scoped>

</style>