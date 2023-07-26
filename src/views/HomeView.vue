<template>
  <v-hover>
    <div class="projects">
      <v-row class="ma-0 mt-10 " @mouseleave="resetHoveredStates">
        <v-col class="pa-0 d-flex justify-end cursor">
          <h1 @mouseover="hasLeftBeenHovered = true; hasRightBeenHovered = false" class="d-flex "
            :class="{ 'webDesignBackground': hasRightBeenHovered, 'backgroundConfig': hasRightBeenHovered }">
            <v-icon class="lessThen backgroundConfig" :class="{ 'webDesignBackground': hasRightBeenHovered }"
              icon="chevron_left"></v-icon>
            PROJ
          </h1>
        </v-col>
        <v-col ref="bgImgWebDesign" class="pa-0 d-flex justify-start cursor">
          <h1 @mouseover="hasRightBeenHovered = true; hasLeftBeenHovered = false"
            class="d-flex backgroundConfig webDesignBackground" :class="{ 'codingBackground': hasLeftBeenHovered }">
            ECTS
            <v-icon class="pen backgroundConfig" :class="{ 'codingBackground': hasLeftBeenHovered }" icon="edit"></v-icon>
          </h1>
        </v-col>
        <!-- <v-expand-transition> -->
        <!--  -->
        <div v-if="hasLeftBeenHovered" class="d-flex v-card--reveal text-h2 code">
          <div class="d-flex project-content">
            <div class="namecard">
              <v-title class="py-3 title">Frontend projects</v-title>
            </div>
            <div class="card-project">
              <v-sheet max-width="690">
                <v-slide-group v-model="model" class="pa-4" selected-class="bg-success" show-arrows>
                  <v-slide-group-item v-slot="{ toggle }">
                    <v-card :class="['ma-4']" class="ma-3 d-flex flex-column justify-space-between card" @click="toggle">
                      <div>
                        <img src="../assets/img/world.png" alt="">
                        <v-card-title class="d-flex justify-space-between align-center">
                          <h5>Explore World</h5>
                          <a href=" https://ivanadim.github.io/earth_project/" target="_blank">
                            <i class="fa-brands fa-github custom-icon"></i>
                          </a>
                        </v-card-title>
                      </div>
                      <v-card-subtitle class="pa-0">
                        <v-chip size="small" class="ma-2">JavaScript</v-chip>
                        <v-chip size="small">CSS</v-chip>
                      </v-card-subtitle>
                      <v-card-text class="overflow-auto">
                        <div class="description">Project made in JavaScript that
                          show info about each country in the
                          world.</div>
                      </v-card-text>
                    </v-card>
                  </v-slide-group-item>
                  <v-slide-group-item v-slot="{ toggle }">
                    <v-card :class="['ma-4']" class="ma-3 d-flex flex-column justify-space-between card" @click="toggle">
                      <div>
                        <img src="../assets/img/iq_intaligance.png" alt="">
                        <v-card-title class="d-flex justify-space-between align-center">
                          <h5>IQ Intelligence</h5>
                          <a href="https://ivanadim.github.io/iqintellegence/" target="_blank">
                            <i class="fa-brands fa-github custom-icon"></i>
                          </a>
                        </v-card-title>
                      </div>
                      <v-card-subtitle class="pa-0">
                        <v-chip size="small" class="ma-2">Vue.js</v-chip>
                        <v-chip size="small">Vuetify</v-chip>
                      </v-card-subtitle>
                      <v-card-text class="overflow-auto">
                        <div class="description">Project for a real client made in vue.js.The project is for a translation
                          company.</div>
                      </v-card-text>
                    </v-card>
                  </v-slide-group-item>
                  <v-slide-group-item v-slot="{ toggle }">
                    <v-card :class="['ma-4']" class="ma-3 d-flex flex-column justify-space-between card" @click="toggle">
                      <div>
                        <img src="../assets/img/babyboss.png" alt="">
                        <v-card-title class="d-flex justify-space-between align-center">
                          <h5>Baby's store</h5>
                          <a href="https://ivanadim.github.io/babyboss/" target="_blank">
                            <i class="fa-brands fa-github custom-icon"></i>
                          </a>
                        </v-card-title>
                      </div>
                      <v-card-subtitle class="pa-0">
                        <v-chip size="small" class="ma-2">JavaScript</v-chip>
                        <v-chip size="small">Bootstrap</v-chip>
                      </v-card-subtitle>
                      <v-card-text class="overflow-auto">
                        <div class="description">A personal project made local for a children's clothing and toy store
                        </div>
                      </v-card-text>
                    </v-card>
                  </v-slide-group-item>
                  <v-slide-group-item v-slot="{ toggle }">
                    <v-card :class="['ma-4']" class="ma-3 d-flex flex-column justify-space-between card" @click="toggle">
                      <div>
                        <img src="../assets/img/vr.png" alt="">
                        <v-card-title class="d-flex justify-space-between align-center">
                          <h5>Virtual reality</h5>
                          <a href=" https://ivanadim.github.io/vr-project/" target="_blank">
                            <i class="fa-brands fa-github custom-icon"></i>
                          </a>
                        </v-card-title>
                      </div>
                      <v-card-subtitle class="pa-0">
                        <v-chip size="small" class="ma-2">HTML</v-chip>
                        <v-chip size="small">CSS</v-chip>
                      </v-card-subtitle>
                      <v-card-text class="overflow-auto">
                        <div class="description">My first personal project made only with HTML & CSS. This project is
                          about virtual reality.</div>
                      </v-card-text>
                    </v-card>
                  </v-slide-group-item>
                </v-slide-group>
              </v-sheet>
            </div>
          </div>
        </div>
        <!--    -->
        <div v-if="hasRightBeenHovered" class="d-flex v-card--reveal text-h2 web">
          <div class="d-flex project-content">
            <div class="namecard">
              <v-title class="py-3 title">Web Design projects</v-title>
            </div>
            <div class="card-project">
              <v-sheet max-width="690">
                <v-slide-group v-model="model" class="pa-4" selected-class="bg-success" show-arrows>
                  <v-slide-group-item v-slot="{ toggle }">
                    <v-card :class="['ma-4']" class="ma-3 d-flex flex-column justify-space-between card" @click="toggle">
                      <div>
                        <img src="../assets/img/photoshop.png" alt="">
                        <v-card-title class="d-flex justify-space-between align-center">
                          <h5>Drawing School</h5>
                          <a href="https://onedrive.live.com/?authkey=%21AC%5FcnS1TEYxEsKw&cid=317112BD87D0AC62&id=317112BD87D0AC62%2112195&parId=317112BD87D0AC62%2112196&o=OneUp"
                            target="_blank" class="ma-0">
                            <span class="material-symbols-outlined custom-icon">
                              cloud
                            </span>
                          </a>
                        </v-card-title>
                      </div>
                      <v-card-subtitle class="pa-0">
                        <v-chip size="small" class="ma-2">Photoshop</v-chip>
                      </v-card-subtitle>
                      <v-card-text class="overflow-auto">
                        <div class="description">Landing page for drawing school for children. The page is made in
                          Photoshop.</div>
                      </v-card-text>
                    </v-card>
                  </v-slide-group-item>
                  <v-slide-group-item v-slot="{ toggle }">
                    <v-card :class="['ma-4']" class="ma-3 d-flex flex-column justify-space-between card" @click="toggle">
                      <div>
                        <img src="../assets/img/adobexd.png" alt="">
                        <v-card-title class="d-flex justify-space-between align-center">
                          <h5>Movie app</h5>
                          <a href="https://onedrive.live.com/?authkey=%21AC%5FcnS1TEYxEsKw&cid=317112BD87D0AC62&id=317112BD87D0AC62%2112148&parId=317112BD87D0AC62%2112200&o=OneUp"
                            target="_blank" class="ma-0">
                            <span class="material-symbols-outlined custom-icon">
                              cloud
                            </span>
                          </a>
                        </v-card-title>
                      </div>
                      <v-card-subtitle class="pa-0">
                        <v-chip size="small" class="ma-2">AdobeXD</v-chip>
                      </v-card-subtitle>
                      <v-card-text class="overflow-auto">
                        <div class="description">Personal project made in Adobe XD. The project is for movie application.
                        </div>
                      </v-card-text>
                    </v-card>
                  </v-slide-group-item>
                  <v-slide-group-item v-slot="{ toggle }">
                    <v-card :class="['ma-4']" class="ma-3 d-flex flex-column justify-space-between card" @click="toggle">
                      <div>
                        <img src="../assets/img/SalesPage1.png" alt="">
                        <v-card-title class="d-flex justify-space-between align-center">
                          <h5>Sale's page</h5>
                          <a href="https://onedrive.live.com/?authkey=%21AC%5FcnS1TEYxEsKw&cid=317112BD87D0AC62&id=317112BD87D0AC62%2112247&parId=317112BD87D0AC62%2112202&o=OneUp"
                            target="_blank" class="ma-0">
                            <span class="material-symbols-outlined custom-icon">
                              cloud
                            </span>
                          </a>
                        </v-card-title>
                      </div>
                      <v-card-subtitle class="pa-0">
                        <v-chip size="small" class="ma-2">Figma</v-chip>
                        <v-chip size="small">Photoshop</v-chip>
                      </v-card-subtitle>
                      <v-card-text class="overflow-auto">
                        <div class="description">The project is made for SEO and Marketing including several tasks. </div>
                      </v-card-text>
                    </v-card>
                  </v-slide-group-item>
                  <v-slide-group-item v-slot="{ toggle }">
                    <v-card :class="['ma-4']" class="ma-3 d-flex flex-column justify-space-between card" @click="toggle">
                      <div>
                        <img src="../assets/img/fitnessapppng.png" alt="">
                        <v-card-title class="d-flex justify-space-between align-center">
                          <h5>Fitness app</h5>
                          <a href="https://onedrive.live.com/?authkey=%21AC%5FcnS1TEYxEsKw&cid=317112BD87D0AC62&id=317112BD87D0AC62%2112246&parId=317112BD87D0AC62%2112202&o=OneUp"
                            target="_blank" class="ma-0">
                            <span class="material-symbols-outlined custom-icon">
                              cloud
                            </span>
                          </a>
                        </v-card-title>
                      </div>
                      <v-card-subtitle class="pa-0">
                        <v-chip size="small" class="ma-2">Figma</v-chip>
                      </v-card-subtitle>
                      <v-card-text class="overflow-auto">
                        <div class="description">Personal project made in Figma. The project is case study for fitness
                          app.</div>
                      </v-card-text>
                    </v-card>
                  </v-slide-group-item>
                </v-slide-group>
              </v-sheet>
            </div>
          </div>
        </div>
        <!-- </v-expand-transition> -->
      </v-row>
    </div>
  </v-hover>
</template>

<script>
export default {
  name: 'HomeView',
  components: {

  },
  data() {
    return {
      hasLeftBeenHovered: false,
      hasRightBeenHovered: false,
      model: null,

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
.titleVideo {
  font-size: 12px;
}

h4 {
  margin-left: 10px;
  font-size: 12px;
  font-weight: 300;
}


.projects {
  height: 100%;
}

.custom-icon {
  color: rgb(31, 31, 31);
}

.custom-icon:hover {
  color: rgb(30, 30, 111);
}


.card {
  /* border: 5px solid blue; */
  width: 200px !important;
  height: 300px;
  /* display: flex;
  flex-direction: column;
  justify-content: space-between; */
}

.v-responsive__content {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.description {
  font-size: 12px;
  line-height: 0.8rem;
  color: #616161;
}


.web,
.code {
  position: absolute;
  top: 200px;
  /* border: 1px solid red; */
  height: 60% !important;
  width: -webkit-fill-available;
  justify-content: center;

}

.v-card--reveal {
  /* align-items: center; */
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
  background-clip: none;
}

h1 {
  height: fit-content;
  /* border: 1px solid red; */
  font-size: 85px;
  font-weight: bolder;
  padding: 0;
  color: rgb(23, 23, 23);
}

.pen {
  font-size: 75px !important;
  margin-top: 23px;
  margin-left: 25px;
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
  margin-left: 15px;
  font-weight: 800;
}

.card img {
  height: 100px !important;
  width: 100%;
}

.v-card h5 {
  font-size: 16px !important;
}

.v-slide-group__prev,
.v-slide-group__next {
  padding: 50px !important;
}

.project-content {
  /* border: 3px solid blue; */
  width: 80%;
  gap: 40px;
  align-items: flex-end;
  justify-content: space-between;
  border-left: 3px solid #151515;
  border-bottom: 3px solid #151515;
  margin-top: 100px;

}

.namecard {
  width: 30%;
  margin-bottom: 25px;
  /* border: 1px solid blue; */
}

@media screen and (max-width: 1090px) {
  .title {
    font-size: 32px;
    margin-left: 50px;
  }

  .project-content {
    flex-direction: column;
    align-items: flex-start;
  }


  .namecard {
    width: 100%;
    margin-bottom: 0px;
  }

  .v-slide-group__prev,
  .v-slide-group__next {
    padding: 0px !important;
    flex: 0 0 40px !important;
    min-width: 40px !important;
  }

  .card-project {
    /* border: 1px solid red; */
    width: 580px;
  }

  .v-sheet {
    max-width: 580px !important;
  }
}

@media screen and (max-width: 600px) {
  h1 {
    font-size: 40px;
  }

  .title {
    margin: 0;
    font-size: 20px;
  }

  .pen {
    font-size: 40px !important;
    margin-top: 8px;
    margin-left: 12px !important;
  }

  .project-content {

    align-items: center;
    justify-content: space-around;
    margin-top: 0px;
    border: none;
    gap: 0px;
  }

  .card {
    height: 300px;
    width: 200px !important;
  }

  .card-project {
    /* border: 1px solid red; */
    width: 350px;
  }

  .v-sheet {
    max-width: 350px !important;
  }



}
</style>
