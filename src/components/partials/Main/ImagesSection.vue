<template>
    <div class="list-images-container">
        <ul>
            <li v-for="(image, index) in images" :key="index">
                <img :src="require('../../../assets/img/' + image.src)" alt="">
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'ImagesSection',
    data() {
        return {
            images: [
                {
                    src: 'gallery.jpg'
                },
                {
                    src: 'news.jpg'
                },
                {
                    src: 'University_of_Melbourne_autumn.jpg'
                },
                {
                    src: 'small-college-marketing.jpg'
                }
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
    .list-images-container {
        width: 100%;
        height: 33vh;
        ul {
            display: flex;
            height: 100%;
            li {
                width: calc(100% / 4);
                height: 100%;
                list-style: none;

                img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                    object-position: center;
                }
            }
        }
    }
</style>