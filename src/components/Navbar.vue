<template>
    <div class="nav">
        <RouterLink to="./about" class="nav-link">About</RouterLink>
        <RouterLink to="./contact" class="nav-link">Contact</RouterLink>
    </div>
</template>

<script>
import { RouterLink } from 'vue-router';

</script>

<style>
.nav {
    display: flex;
    justify-content: center;
    padding-top: 2%;
    gap: 20px
}

.nav-link {
    position: relative;
    padding: 4px 8px;
    border-radius: 5px;
    font-weight: 700;
    display: inline-block;
    margin-right: 10px;
    color: rgb(67, 67, 67);
    text-decoration: none;
    transition: color 0.5s ease-in-out;
}


.nav-link:hover {
    color: #f2f2f2;
}

.nav-link::before {
    background: #313131;
    content: "";
    inset: 0;
    position: absolute;
    transform: scaleX(0);
    transform-origin: right;
    transition: transform 0.5s ease-in-out;
    z-index: -1;
    border-radius: 5px;

}

.nav-link:hover::before {
    transform: scaleX(1);
    transform-origin: left;
}

@media screen and (max-width: 550px) {
    .nav-link {
        font-size: 14px;
    }
}
</style>
