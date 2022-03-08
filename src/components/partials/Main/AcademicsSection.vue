<template>
    <div class="academics-container">
        <a name="Academics"></a>
        <div
        class="text"
        :style="{
                    backgroundImage: 'url(' + require('../../../assets/img/quote.png') + ')'
                }">

            <p>"Academics was committed to my successfrom the moment I attended an Open House. With the support of caring <font color="#D74D52"><u><b>advisors, professors, and staff</b></u></font> i was able to thrive in courses, gain recognition through scholarships, and finish <b>with confidence in my abilities <font color="#D74D52"><u>@academics </u></font>abilities</b> </p>
        </div>
        <div class="img-overlying">
            <div
            class="box-img"
            :style="{
                    backgroundImage: 'url(' + require('../../../assets/img/video-bg-3.jpg') + ')'
                }"
            >
                <div class="play">
                    <span>&#9655;</span>
                </div>

            </div>
            <div class="box-overlying">
                <div class="red-label">
                    <p>Upcoming Events</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AcademicsSection'
}
</script>

<style lang="scss" scoped>
    .academics-container {
        width: 60%;
        height: 100vh;

        .text {
            display: flex;
            align-items: center;
            margin: 5% 0;
            width: 100%;
            height: 20%;
            line-height: 1.5;
            text-align: center;
            font-size: 160%;
            background-size: fill;
            background-position: center;
            background-repeat: no-repeat;
        }
        .img-overlying {
            position: relative;
            width: 60%;
            height: 50%;
            .box-img {
                display: flex;
                justify-content: center;
                align-items: center;
                width: 100%;
                height: 100%;
                background-image: cover;
                background-position: center;


                .play {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    
                    span {
                        font-size: 2.5rem;
                        padding: 5px;
                        color: #d74d52;
                        background-color: white;
                        border-radius: 20%;
                    }
                }
            }

            .box-overlying {
                position: absolute;
                top: 15%;
                left: 65%;
                width: 100%;
                height: 100%;
                background-color: white;
                box-shadow: 0px 5px 5px 0px rgb(240, 240, 240);

                .red-label {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    margin: 0 auto;
                    width: 50%;
                    height: 20%;
                    font-size: 150%;
                    color: white;
                    background-color: #d74d52;

                }
            }
        }
    }
</style>