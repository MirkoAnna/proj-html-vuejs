<template>
    <div class="container">

        <SubscribeComponent />


        <div class="menu-container">

            <MenuFooter title="Contact Us" :items="contactUs"/>
            <MenuFooter title="Support US" :items="supportUs"/>
            <MenuFooter title="Explore" :items="explore"/>
            <MenuFooter title="Visit" :items="visit"/>

        </div>


        <FooterEnd />


        <div class="square">

        </div>
    </div>
</template>

<script>
import SubscribeComponent from './partials/Footer/SubscribeComponent.vue';
import MenuFooter from './partials/Footer/MenuFooter.vue';
import FooterEnd from './partials/Footer/FooterEnd.vue';
export default {
    name: 'MyFooter',
    components: {
        SubscribeComponent,
        MenuFooter,
        FooterEnd
    },
    data() {
        return {
            contactUs: [
                {
                    src: "#",
                    text: "900 Wood Street, MI New York 48607",
                    icon: "fa-solid fa-location-dot"
                },
                {
                    src: "#",
                    text: "+56 345 678 000-09",
                    icon: "fa-solid fa-square-phone"
                },
                {
                    src: "#",
                    text: "info@example.com",
                    icon: "fa-solid fa-envelope"
                }
            ],
            supportUs: [
                {
                    src: "#",
                    text: "Privacy"
                },
                {
                    src: "#",
                    text: "Terms"
                },
                {
                    src: "#",
                    text: "Cookie Policy"
                },
                {
                    src: "#",
                    text: "Sitemap"
                }
            ],
            explore: [
                {
                    src: "#",
                    text: "Accommodation"
                },
                {
                    src: "#",
                    text: "Arts Academics"
                },
                {
                    src: "#",
                    text: "Central Services"
                },
                {
                    src: "#",
                    text: "Conferences and Events"
                },
                {
                    src: "#",
                    text: "Food and Drink"
                }
            ],
            visit: [
                {
                    src: "#",
                    text: "Admission"
                },
                {
                    src: "#",
                    text: "Contact Us"
                },
                {
                    src: "#",
                    text: "FAQs"
                },
                {
                    src: "#",
                    text: "Request Information"
                },
                {
                    src: "#",
                    text: "Privacy Notice"
                }
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
    .container {
        position: relative;
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100%;
        height: 65vh;
        font-size: 65%;
        color: $footerText;
        background-color: $primaryFooter;

        .menu-container {
            display: flex;
            width: 60%;
            height: 46%;
        }

        .square {
            position: absolute;
            bottom: 12%;
            right: 2%;
            width: 1.8rem;
            height: 1.8rem;
            background-color: rgb(204, 204, 204);
        }
    }
</style>