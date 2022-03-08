<template>
    <div class="main-container">
        <AboutSection />

        <CoursesSection/>

        <AcademicsSection />
        
        <ImagesSection />
    </div>
</template>

<script>
import AboutSection from './partials/Main/AboutSection.vue';

import CoursesSection from './partials/Main/CoursesSection.vue';

import AcademicsSection from './partials/Main/AcademicsSection.vue';

import ImagesSection from './partials/Main/ImagesSection.vue';

export default {
    name: 'MyMain',
    components: {
        AboutSection,
        CoursesSection,
        AcademicsSection,
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