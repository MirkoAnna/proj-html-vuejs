<template>
    <div class="container-footer-end">
        <p>&copy; Copyright 2020 tophive. All right reserved.</p>
        <ul>
            <li v-for="(link, index) in links" :key="index">
                <a href="#">{{link.text}}</a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'FooterEnd',
    data() {
        return {
            links: [
                {
                    text: 'Privacy',
                    url: '#'
                },
                {
                    text: 'Terms',
                    url: '#'
                },
                {
                    text: 'Cookie Policy',
                    url: '#'
                },
                {
                    text: 'Sitemap',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../../assets/style/variables.scss';

    .container-footer-end {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        height: 8%;
        background-color: #15222E;

        p {
            text-align: right;
            width: 35%;
        }
        ul {
            display: flex;
            justify-content: center;
            width: 60%;

            li {
                display: flex;
                list-style: none;
                margin-right: 4%;

                a {
                    text-decoration: none;
                    color: $footerText;
                }
            }
        }
    }
</style>