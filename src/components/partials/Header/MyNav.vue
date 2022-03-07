<template>
    <nav>
        <div class="logo">
            <img src="../../../assets/img/Logo.jpg" alt="">
        </div>

        <ul>
            <li v-for="(link, index) in links" :key="index">
                <a :href="link.url">{{link.text}}</a>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
    name: 'MyNav',
    props: {
        "links": Array
    }
}
</script>

<style lang="scss" scoped>
@import '../../../assets/style/variables.scss';
    nav {
        display: flex;
        justify-content: space-between;
        position: fixed;
        top: 0;
        width: 99%;
        height: 8vh;
        background-color: white;
        z-index: 1;
        ul {
            display: flex;
            width: 40%;
            height: 100%;
            li {
                display: inline;
                margin-right: 3.5%;
                line-height: 8vh;
                height: 100%;
                
                a {
                    font-size: 76%;
                    font-weight: 600;
                    text-decoration: none;
                    color: $primaryText;
                    height: 100%;

                }
                &:hover {
                    border-bottom: 2px solid #D74D52;
                }
            }
        }
        .logo {
            width: 30%;
            text-align: right;
            img {
                height: 5rem;
            }
        }
    }
</style>