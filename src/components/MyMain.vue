<template>
    <div class="main-container">
        <AboutSection />
        <ImagesSection />
    </div>
</template>

<script>
import AboutSection from './partials/Main/AboutSection.vue';
import ImagesSection from './partials/Main/ImagesSection.vue';
export default {
    name: 'MyMain',
    components: {
        AboutSection,
        ImagesSection
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";

    .main-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100%;
        color: $primaryText;
    }
</style>