<template>
    <div class="about-container">
        <a name="About"></a>
        <h2> Since 2000, weve been partnering with education leaders to <font color=#D74D52>increase equity and achievement</font> for all students.</h2>

        <ul class="card-container">
            <li class="card" v-for="(card, index) in cards" :key="index">
                <img :src="require('../../../assets/svg/' + card.src)" alt="">
                <p>{{card.title}}</p>
                <p>{{card.text}}</p>
            </li>
        </ul>

        <ul class="statistics-container">
            <li class="statistic" v-for="(statistic, index) in statistics" :key="index">
                <div 
                class="statistic-image"
                :style="{
                            'background-image': 'url(' + require('../../../assets/img/' + statistic.src) + ')'
                        }">

                    <h2><font :color="statistic.color">{{statistic.statistic}}</font></h2>

                </div>

                <span>{{statistic.text}}</span>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name:'AboutSection',
    data() {
        return {
            cards: [
                {
                    src: 'svg-0.svg',
                    title: 'Online Coaching',
                    text: 'Lorem ipsum is simply dummy text of the print ing and typesetting has been the industrys'
                },
                {
                    src: 'svg-1.svg',
                    title: 'Consultation',
                    text: 'Lorem ipsum is simply dummy text of the print ing and typesetting has been the industrys'
                },
                {
                    src: 'svg-2.svg',
                    title: 'Life Programs',
                    text: 'Lorem ipsum is simply dummy text of the print ing and typesetting has been the industrys'
                }
            ],
            statistics: [
                {
                    src: 'counter-shape-1-1-1.png',
                    statistic: '6500 +',
                    text: 'Students',
                    color: '#F28202'
                },
                {
                    src: 'counter-shape-2-1-1.png',
                    statistic: '200 +',
                    text: 'Online Courses',
                    color: 'D74D52'
                },
                {
                    src: 'counter-shape-3-1-1.png',
                    statistic: '100 %',
                    text: 'Happy Clients',
                    color: '#3ADC79'
                }
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
    .about-container {
        margin: 2% 0;
        width: 60%;
        height: 75vh;
        text-align: center;

        h2 {
            line-height: 1.5;
            font-size: 165%;
        }
        .card-container {
            display: flex;
            margin: 7% 0;
            width: 100%;
            height: 45%;
            .card {
                display: flex;
                flex-direction: column;
                justify-content: center;
                justify-content: space-around;
                margin: 0 0.9%;
                padding: 2.5%;
                width: calc(99% / 3);
                height: 100%;
                line-height: 1.5;
                font-size: 87%;
                text-align: center;
                list-style: none;
                box-shadow: 0px 5px 5px 5px rgb(240, 240, 240);
                

                p:first-of-type {
                    font-weight: 600;
                }
                img {
                    margin: 0 auto;
                    width: 3rem;
                    height: 3rem;
                }
            }
        }
        .statistics-container {
            display: flex;
            width: 100%;
            height: 10%;

            .statistic {
                display: flex;
                align-items: center;
                margin: 0 0.9%;
                width: calc(99% / 3);
                height: 100%;
                list-style: none;

                .statistic-image {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    width: 40%;
                    height: 100%;
                    font-size: 120%;
                    background-repeat: no-repeat;
                    background-size: contain;
                    background-position: center;
                }
                span {
                    font-weight: 600;
                }
            }
        }
    }
</style>