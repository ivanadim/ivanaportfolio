<template>
    <router-link class="home" :to="{ name: 'home' }"><v-icon class="home-icon" icon="arrow_back"></v-icon>
    </router-link>
    <div class="contact">
        <div class="title text-center">
            <h1>"Let's Begin This Story Together"</h1>
        </div>
        <div class="description">
            <p> Drop me a line at <a href="mailto:ivana.n03i@gmail.com" class="email">ivana.n03i@gmail.com</a> to start our
                collaborative journey towards creating something extraordinary.
                Whether you have a question, an exciting project idea, or just want to say hello, I'm eager to hear from
                you. Let's bring our creativity together and make magic happen! I can't wait to connect with you,
                collaborate on exciting projects, and make our shared story an
                unforgettable one. </p>
            <br>
            <p>
                To explore my projects and get a glimpse into my creative world, feel free to visit the following platforms:
            <ul>
                <li> <a href="https://www.linkedin.com/in/ivana-dimitrova-253656253/" target="_blank"><i
                            class="fa-brands fa-linkedin-in fa-shake fa-xl d-flex align-center icon" target="_blank"></i>
                        <h4>Linkedin</h4>
                    </a>
                </li>
                <li><a href="https://github.com/ivanadim" target="_blank">
                        <i class="fa-brands fa-github fa-shake fa-xl d-flex align-center icon"></i>
                        <h4>GitHub</h4>
                    </a>
                </li>
                <li> <a href="https://www.instagram.com/iddesign3333/" target="_blank"><i
                            class=" fa-brands fa-square-instagram fa-shake fa-xl d-flex align-center icon"></i>
                        <h4>Instagram</h4>
                    </a>
                </li>
                <li> <a href="https://www.behance.net/ivananikolova1" target="_blank"> <i
                            class="fa-brands fa-square-behance fa-shake fa-xl d-flex align-center icon"></i>
                        <h4>Behance</h4>
                    </a></li>
            </ul>
            </p>
            <p>Reach out via email, explore my projects on GitHub and Behance, and let's embark on this
                journey together.</p>
        </div>
    </div>
</template>
<script>

</script>
<style scoped>
h4 {
    font-size: 1rem;
    font-weight: 500;
}

.contact {
    /* border: 1px solid blue; */
    height: 85%;
    padding: 7% 10% 4%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.title h1 {
    color: #313131;
    font-family: 'Comforter Brush', cursive;
    font-size: 100px;
    font-weight: 700;
    line-height: 90px;
    margin-bottom: 20px
}

.description {
    font-family: 'Open Sans';
    line-height: 1.8rem;
    font-weight: 400;
    font-size: 1rem;
    padding: 0px 2%;
}

.description ul {
    list-style: none;
    /* border: 1px solid red; */
    margin: 10px 30px 0px;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    /* gap: 5%; */
}

.description ul li {
    height: 40px;
    display: flex;
    align-items: center;
    width: 47%;
    /* border: 1px solid green; */
    margin-bottom: 2%;
    /* padding-left: 20px; */
    border-left: 3px solid #313131;
    /* border: 1px solid #313131; */

}

.description ul li a {
    position: relative;
    display: inline-block;
    text-decoration: none;
    color: #313131;
    display: flex;
    gap: 10px;
    height: 40px;
    align-items: center;
    border-radius: 0px 5px 5px 0px;
    /* border: 1px solid red; */
    padding: 5px 10px 5px 20px;
    transition: color 0.5s ease-in-out;
}

.description ul li a:hover {
    /* background-color: #313131; */
    color: #f2f2f2;
}

.description ul li a::before {
    background: #313131;
    content: "";
    inset: 0;
    position: absolute;
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.5s ease-in-out;
    z-index: -1;
    border-radius: 0px 5px 5px 0px;
}

.description ul li a:hover:before {
    transform: scaleX(1);
    transform-origin: left;
}

.email {
    background-color: #313131;
    padding: 5px 10px;
    border-radius: 5px;
    color: #f2f2f2;
    font-weight: bolder;
}

@media screen and (max-width: 1090px) {
    .contact {
        padding-top: 15%;
    }
}

@media screen and (max-width: 600px) {
    .contact {
        padding-top: 10%;
    }

    .title h1 {
        font-size: 42px !important;
        padding-left: 0px;
        line-height: normal;
        /* padding-bottom: 20px; */
    }

    .description {
        font-size: 10px;
        line-height: 18px;
    }

    .description ul {
        margin: 20px 0px 10px 0px;
    }

    .description ul li {
        height: 30px;
    }

    .description ul li a {
        padding: 5px 10px;
        height: 30px;
    }

    h4 {
        margin-left: 5px;
        font-size: 14px;
        font-weight: 700;
    }
}
</style>