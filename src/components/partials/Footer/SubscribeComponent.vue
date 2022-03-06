<template>
    <div class="subscribe-container">
        <div class="box">
            <div class="subscribe">
                <input type="text" placeholder="Subscribe to our newsletter">
                <button>Register</button>
            </div>
            
            <div class="text">
                <p><a href="">Insights is Picwik</a> University's thought leadership publication for sharing knowledge on management, technology and innovation.</p>
                <p><a href="#">Take me there <font size="3">&rsaquo;</font></a></p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:'SubscribeComponent.vue'
}
</script>

<style lang="scss" scoped>
@import '../../../assets/style/variables.scss';

    .subscribe-container {
        display: flex;
        align-items: center;
        margin: 0 auto;
        width: 60%;
        height: 46%;

        .box {
            display: flex;
            align-items: center;
            width: 100%;
            height: 50%;
            box-shadow: 0px 0px 5px 5px #15222E;

            .subscribe {
                display: flex;
                justify-content: center;
                width: 50%;
                height: 55%;
                padding: 1% 0;
                border-left: 5px solid #23374B;

            }
            input {
                padding: 3%;
                width: 55%;
                height: 100%;
                font-size: 90%;
            }
            button {
                width: 25%;
                color: white;
                border: none;
                background-color: $mattRed;
                font-size: 90%;

                &:hover {
                    cursor: pointer;
                    border: 1px solid #15222E;
                }
            }

            .text {
                padding: 1% 2%;
                width: 50%;
                height: 55%;

                u {
                    text-decoration-color: white;
                    color: $mattRed;
                }

                p:first-child a {
                    font-weight: 600;
                    text-decoration-color: white;
                    color: $mattRed;
                }
                p:last-child {
                    padding-top: 2%;

                    a {
                        font-weight: 600;
                        text-decoration: none;
                        color: white;
                        font {
                            font-weight: none;
                        }
                    }
                }
            }
        }
    }
</style>
