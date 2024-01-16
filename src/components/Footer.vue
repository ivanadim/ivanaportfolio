<template>
    <div class="footer">
        <div class="bg-white d-flex justify-center w-100 social-icon">
            <a href="https://github.com/ivanadim" target="_blank"><i
                    class="fa-brands fa-github fa-xl d-flex align-center icon"></i></a>
            <a href="https://www.linkedin.com/in/ivana-dimitrova-253656253/" target="_blank"><i
                    class="fa-brands fa-linkedin-in  fa-xl d-flex align-center icon" target="_blank"></i></a>
            <a href="https://www.instagram.com/iddesign3333/" target="_blank"><i
                    class=" fa-brands fa-square-instagram  fa-xl d-flex align-center icon"></i></a>
            <a href="https://www.behance.net/ivananikolova1" target="_blank"> <i
                    class="fa-brands fa-square-behance  fa-xl d-flex align-center icon"></i></a>
        </div>
    </div>
</template>

<script>

export default {

}
</script>

<style scoped>
.social-icon {
    gap: 20px;
    height: 50px;
}

.social-icon a .icon {
    width: 40px;
    height: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 10px;
    border-radius: 50%;
    transition: all 0.2s ease-in-out;
    cursor: pointer;
    margin-right: 10px;
    color: #000000;
}

.social-icon a {
    text-decoration: none;
}

a .icon:hover {
    /* background-image: url("../assets/img/web-design.jpg"); */
    background: #000000;
    color: #FFFFFF;
}

@media screen and (max-width: 550px) {
    .social-icon {
        gap: 10px;
    }
}
</style>