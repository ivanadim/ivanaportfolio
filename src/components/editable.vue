<template>
    <v-app>
        <v-main style="position: relative;">
            <v-hover v-slot="{ isHovering, props }">
                <v-row class="ma-0 mt-10 " v-bind="props" @mouseleave="resetHoveredStates">
                    <v-col class="pa-0 d-flex justify-end cursor">
                        <h1 @mouseover="hasLeftBeenHovered = true; hasRightBeenHovered = false" class="d-flex "
                            :class="{ 'webDesignBackground': hasRightBeenHovered, 'backgroundConfig': hasRightBeenHovered }">
                            <v-icon class="lessThen backgroundConfig"
                                :class="{ 'webDesignBackground': hasRightBeenHovered }" icon="chevron_left"></v-icon>
                            PROJ
                        </h1>
                    </v-col>
                    <v-col ref="bgImgWebDesign" class="pa-0 d-flex justify-start cursor">
                        <h1 @mouseover="hasRightBeenHovered = true; hasLeftBeenHovered = false"
                            class="d-flex backgroundConfig webDesignBackground"
                            :class="{ 'codingBackground': hasLeftBeenHovered }">
                            ECTS
                            <v-icon class="ml-5 pen backgroundConfig" :class="{ 'codingBackground': hasLeftBeenHovered }"
                                icon="edit"></v-icon>
                        </h1>
                    </v-col>
                    <v-expand-transition>
                        <div v-if="isHovering && hasLeftBeenHovered"
                            class="d-flex transition-fast-in-fast-out v-card--reveal text-h2 code" style="height: 80%">
                            <div class="d-flex flex-column justify-center">
                                <v-title class="py-3 title">Frontend projects</v-title>
                                <v-carousel height="300" width="600" hide-delimiters class="slider">
                                    <v-carousel-item cover>
                                        <!-- <img src="../assets/img/world.png" alt="world">
                       -->
                                        <video width="600" height="250" autoplay>
                                            <source src="../assets/img/World.mp4" type="video/mp4">
                                        </video>
                                        <div>
                                            <h4>Explore World</h4>
                                        </div>

                                    </v-carousel-item>
                                    <v-carousel-item src="../assets/img/babyboss.png" cover><img
                                            src="../assets/img/iq_intaligance.png" alt="iq"></v-carousel-item>

                                    <v-carousel-item src="../assets/img/babyboss.png" cover><img
                                            src="../assets/img/babyboss.png" alt="babyboss"></v-carousel-item>
                                </v-carousel>
                            </div>
                        </div>

                        <div v-if="isHovering && hasRightBeenHovered"
                            class="d-flex  transition-fast-in-fast-out v-card--reveal text-h2 web">
                            <v-title class="py-3 title">Web Design projects</v-title>
                        </div>
                    </v-expand-transition>
                </v-row>
            </v-hover>

        </v-main>
        <Footer></Footer>
    </v-app>
</template>
  
<script>
import Footer from '../components/Footer.vue'
export default {
    name: 'HomeView',
    components: {
        Footer
    },
    data() {
        return {
            hasLeftBeenHovered: false,
            hasRightBeenHovered: false
        }
    },

    methods: {
        resetHoveredStates() {
            this.hasLeftBeenHovered = false;
            this.hasRightBeenHovered = false;
        }
    }
};

</script>
  
<style>
.v-carousel {
    border: 1px solid gold;
}

.v-main {
    height: 60% !important;
    border: 2px solid green;
}

.slider {
    width: 650px !important;
}

.slider img {
    background-size: cover !important;
    width: 100%;
}

.slider p {
    color: black;
}

.web,
.code {
    position: absolute;
    top: 170px;
    border: 1px solid red;
    height: 500px !important;
}

.v-card--reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: .9;
    position: absolute;
    width: 100%;
}

.backgroundConfig {
    background-size: contain;
    background-repeat: repeat;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

h1 {
    height: fit-content;
    /* border: 1px solid red; */
    font-size: 102px;
    font-weight: bolder;
    color: rgb(23, 23, 23);
}

.pen {
    font-size: 82px !important;
    margin-top: 30px;
    margin-left: 10px;
    background-image: url("../assets/img/web-design.jpg");

}

.lessThen {
    background-image: url("../assets/img/front-end.jpg");
}

.codingBackground {
    background-image: url("../assets/img/front-end.jpg") !important;
    /* font-family: 'Open Sans', sans-serif; */
}

.webDesignBackground {
    background-image: url("../assets/img/web-design.jpg");
    /* font-family: 'Open Sans', sans-serif; */
}

.cursor {
    cursor: pointer;
}

.title {
    font-family: 'Open Sans', sans-serif;
    font-size: 24px;
    font-weight: 800;
}
</style>