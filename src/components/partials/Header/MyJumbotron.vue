<template>
    <div class="jumbotron" 
        :style="{
                    backgroundImage: 'url(' + require('../../../assets/img/02_Landing-Page.jpg') + ')'
                }"
    >
        <div class="text">
            <p>professional development for coaches and leaders</p>
            <button>Learn More</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MyJumbotron'
}
</script>

<style lang="scss" scoped>
@import '../../../assets/style/variables.scss';

    .jumbotron {
            width: 100%;
            height: 100vh;
            background-repeat: no-repeat;
            background-size: cover;
            background-position: center;
        }
        .text {
            position: absolute;
            top: 43%;
            left: 50%;
            width: 35;
            text-align: center;
            text-transform: capitalize;
            font-size: 280%;
            transform: translate(-50%, -50%);

            button {
                margin-top: 6%;
                padding: 1.5%;
                width: 20%;
                font-size: 0.7rem;
                color: $primaryText;
                border: 1px solid #CCCCCC;
                background-color: rgba(255, 255, 255, 0);

                &:hover {
                    cursor: pointer;
                    scale: 1.1;
                }
            }
        }
</style>