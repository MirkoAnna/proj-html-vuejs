<template>
    <div class="courses-container">
        <a name="Courses"></a>
        <div class="title-text">
            <h2>Recent Courses</h2>
            <p>Wether you're considering a foundation course or an undergraduate degree master's or a PhD, academics is a place where students thrive.</p>
        </div>
        <ul class="courses-box">
            <li class="course" v-for="(course, index) in courses" :key="index">
                <div class="course-image">
                    <img :src="require('../../../assets/img/' + course.src)" alt="">
                </div>
                <div class="course-text">
                    <p>{{course.submission}}</p>
                    <h3>{{course.title}}</h3>
                    <p>{{course.text}}</p>
                    <p>{{course.by}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'CoursesSection',
    data() {
        return {
            courses: [
                {
                    src: 'bruce-mars-FWVMhUa_wbY-unsplash.jpg',
                    submission: 'Free',
                    title: 'UI Animation using Sketch 3, Principle App, and Flinto',
                    text: 'This online photography course will teach you how to take amazing images and even sell...',
                    by: 'Courses by : University'
                },
                {
                    src: 'course-1-2.jpg',
                    submission: 'Free',
                    title: 'The Ultimate Drawing Course - Begginer to Advanced',
                    text: 'This online photography course will teach you how to take amazing images and even sell...',
                    by: 'Courses by : University'
                },
                {
                    src: 'william-thomas-ny6tO4ItOEY-unsplash.jpg',
                    submission: 'Free',
                    title: 'Your Complete Guide to Photography',
                    text: 'This online photography course will teach you how to take amazing images and even sell...',
                    by: 'Courses by University'
                }
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../../assets/style/variables.scss';

    .courses-container {
        width: 71%;
        height: 75vh;

        .title-text {

            text-align: center;
            h2 {
                font-size: 165%;
            }

            p {
                margin: 2% auto;
                text-align: center;
                line-height: 1.5;
                width: 60%;
            }
        }
            .courses-box {
                display: flex;
                justify-content: center;
                margin: 5% auto;
                width: 100%;
                height: 70%;

                .course {
                    display: flex;
                    flex-direction: column;
                    margin: 0 1.2%;
                    width: calc(88% / 3);
                    height: 100%;
                    line-height: 1.5;
                    font-size: 87%;
                    list-style: none;
                    box-shadow: 0px 5px 5px 5px rgb(240, 240, 240);

                    &:hover {
                        scale: 1.1;
                        cursor: pointer;
                    }

                    .course-image {
                        width: 100%;
                        height: 36%;
                        img {
                            width: 100%;
                            height: 100%;
                        }
                    }
                    .course-text {
                        display: flex;
                        flex-direction: column;
                        justify-content: space-around;
                        width: 94%;
                        height: 100%;
                        padding: 7%;

                        p:first-of-type {
                            line-height: 0.6rem;
                            width: 1.8rem;
                            background: linear-gradient(to bottom,
                            white 50%, rgba(204, 0, 0, 0.2) 50%);
                        }
                        p:last-of-type {
                            margin-top: 2%;
                            font-size: 0.7rem;
                            color: $mattRed;
                        }
                    }
                }
            }
    }
</style>