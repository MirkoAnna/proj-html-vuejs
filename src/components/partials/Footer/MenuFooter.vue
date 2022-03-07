<template>
    <div class="container-object">
        <h2>{{title}}</h2>
        <nav>
            <ul>
                <li v-for="(item, index) in items" :key="index">
                    <div v-if="item.icon">
                        <a :href="item.src"><i :class="item.icon"></i>{{item.text}}</a>
                    </div>
                    <div v-else>
                        <a :href="item.src">&rsaquo; {{item.text}}</a>
                    </div>
                </li>
            </ul>
        </nav>
    </div>
</template>

<script>
export default {
    name: 'MenuFooter',
    props: ["title", "items"]
}
</script>

<style lang="scss" scoped>
@import '../../../assets/style/variables.scss';

    .container-object {
        display: flex;
        flex-direction: column;
        width: calc(100% / 4);
        h2 {
            color: white;
        }
        nav {

            ul{
                li {
                    margin: 6% 0;
                    width: 64%;
                    list-style: none;
                    a {
                        text-decoration: none;
                        color: $footerText;

                        &:hover {
                            text-decoration: underline;
                        }

                        i {
                            margin-right: 4%;
                        }
                    }
                }
            }
        }
    }
</style>