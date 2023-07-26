<template>
    <router-link class="home" :to="{ name: 'home' }"><v-icon class="home-icon" icon="arrow_back"></v-icon></router-link>
    <div class="bg">
        <div class="about">
            <div class="imagepart">
                <div class="image">
                    <!-- <img src="../assets/img/ivana1bw.png" alt=""> -->
                </div>
                <v-title class="title d-sm-none">Ivana <br> Dimitrova
                </v-title>
            </div>
            <div class="text">
                <v-title class="title d-none d-sm-flex">Ivana
                    <br> Dimitrova
                </v-title>
                <v-text class="content mt-10 w-100">
                    Hi there. I have been interested in creativity all my life. I am very sensitive to each project
                    and
                    i
                    always try to find a compromise on any issue.
                    I design, build and operate solution and digital strategies for all needs.
                </v-text>
                <a href="https://1drv.ms/b/s!AmKs0Ie9EnEx31R3Uq_G-YtHqtdK" target="_blank">
                    <button type="button">
                        DOWNLOAD MY CV</button></a>
            </div>
        </div>
    </div>
</template>

<style scoped>
.bg {
    height: 80%;
    display: flex;
    flex-direction: column;
    padding-bottom: 30px;
    align-items: center;
}

.about {
    /* position: relative; */
    justify-content: space-between;
    height: 100%;
    display: flex;
    align-items: flex-end;
    /* border: 1px solid red; */
    margin: 8% 8% 0% 8%;
    border-left: 3px solid #151515;
    border-bottom: 3px solid #151515;
}

.image img {
    height: 300px !important;
    /* border-bottom: 3px solid #151515;
    border-left: 3px solid #151515; */
}

.text {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: flex-start;
    height: 100%;
    /* border: 2px solid green; */
    padding: 0% 10%;
    width: 70%;
}

.title {
    font-family: 'Comforter Brush', cursive;
    font-size: 100px;
    font-weight: 500;
    line-height: 90px;
}

.content {
    font-family: 'Open Sans';
    font-size: 1.1rem;
    font-weight: 500;
}

.image {
    background-image: url("../assets/img/ivana1bw.png");
    background-size: cover;
    background-position: bottom;
    height: 100%;
    /* border: 1px solid blue; */
    display: flex;
    align-items: flex-end;
    width: 100%;
    /* margin-bottom: 1px; */
    transform: scaleX(-1);
}

a button {
    font-family: 'Open Sans';
    font-weight: 700;
    background-color: #151515;
    color: #f2f2f2 !important;
    padding: 8px 16px;
    border-radius: 8px;
    border: 1px solid #151515;
    transition: color 0.3s ease-in-out;
}

a button:hover {
    background-color: #f2f2f2;
    color: #151515 !important;
}

.imagepart {
    width: 40%;
    height: 100%;
}

@media screen and (max-width: 1090px) {
    .bg {
        height: 70%;
    }

    .text {
        width: 60%;
    }

    .title {
        margin-left: 10px;
    }

    .imagepart {
        width: 40%;
        height: 100%;
    }

    .image {
        height: 100%;
        width: 100%;
    }
}

@media screen and (max-width: 600px) {
    .bg {
        height: 80%;
        padding-bottom: 10px;
    }

    .about {
        border: none;
        flex-direction: column;
        align-items: center;
    }

    .text {
        width: 100%;
    }

    .content {
        font-size: 12px;
        margin-top: 5px !important;
    }

    a button {
        font-size: 12px;
        margin-top: 15px;
    }

    .title {
        font-size: 40px;
        line-height: normal;
        margin: 0;
    }

    .imagepart {
        display: flex;
        width: 100%;
        height: 500px;
        align-items: flex-end;
        justify-content: space-around;
    }

    .image {
        height: 100%;
        width: 40%;
    }
}
</style>
