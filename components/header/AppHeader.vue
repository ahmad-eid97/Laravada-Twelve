<template>
    <header :class="!topOfPage ? 'onScroll' : ''" class="header header-style-2 clearfix">
        <div class="row m-0 w-100">
            <app-top-bar class="col-12"></app-top-bar>
            <b-navbar toggleable="lg">
                <b-navbar-brand href="#">
                    <img src="/assets/images/logo.png" alt="logoImage">
                </b-navbar-brand>

                <b-navbar-toggle target="navbar-toggle-collapse">
                    <template #default="{ expanded }">
                        <span class="menu-trigger" :class="expanded ? 'active' : ''" id="menu03">
                            <p></p>
                            <p></p>
                            <p></p>
                        </span>
                    </template>
                </b-navbar-toggle>

                <b-collapse id="navbar-toggle-collapse" class="ml-auto justify-content-end navo" is-nav>
                    <b-navbar-nav class="align-items-center">
                        <b-nav-item :to="localePath('/')">Home</b-nav-item>
                        <b-nav-item :to="localePath('/about')">About</b-nav-item>
                        <b-nav-item :to="localePath('/team')">Team</b-nav-item>
                        <b-nav-item :to="localePath('/services')">Services</b-nav-item>
                        <b-nav-item :to="localePath('/testimonials')">Projects</b-nav-item>
                        <b-nav-item :to="localePath('/blogs')">News & articles</b-nav-item>
                        <b-nav-item :to="localePath('/contact')">Contact</b-nav-item>
                        <a href="#" @click="side = !side" class="btn">
                            <font-awesome-icon icon="fa-solid fa-bag-shopping" />
                            <span class="d-lg-none d-block">Side Bar</span>
                        </a>
                    </b-navbar-nav>
                </b-collapse>
            </b-navbar>
            <div :class="side ? 'opend' : '' " @click.self="side = !side" class="side-bar">
                <div class="content-wrapper">
                    <div class="close-btn">
                        <font-awesome-icon icon="fa-solid fa-xmark" @click="side= !side"/>
                    </div>
                    <div class="widge">
                        <p>	
                            No products in the cart.
                        </p>
                    </div>

                </div>
            </div>
        </div>
    </header>
</template>

<script>
import AppTopBar from './AppTopBar.vue'
export default {
    name: 'AppHeader',
    components: {
        AppTopBar,
    },
    data() {
        return {
            side: false,
            topOfPage: true
        }
    },
    beforeMount() {
        window.addEventListener('scroll', this.handleScroll)
    },
    mounted() {
    },
    methods: {
        handleScroll(){
            if(window.pageYOffset>30){
                if(this.topOfPage) this.topOfPage = false
            } else {
                if(!this.topOfPage) this.topOfPage = true
        }
        }
    }
}
</script>
<style lang="scss">
    header {
        position: fixed;
        left: 0;
        right: 0;
        z-index: 10;
        background: transparent;
    }
    .onScroll {
        position: fixed;
        width: 100%;
        padding: 20px 0;
        // height: 70px;
        display: flex;
        align-items: center;
        transition: all .2s ease-in-out;
        box-shadow: 0 0 10px #aaa;
        background-color: #fff;
        top: 0;
        z-index: 1000;
    }
    .onScroll .top-bar {
        overflow: hidden;
        height: 0px;
        padding: 0px;
    }
    .onScroll .social-icon {
        display: none;
    }
    nav {
        padding: 20px 60px 0 !important;
    }
    .onScroll nav {
        padding: 0 60px 0 !important;
    }
    .navbar-brand {
        width: 180px;
        transition: all 0.3s linear;

    }
    .onScroll .navbar-brand {
        width: 140px;

    }
    .navbar .nav-item {
        margin: 0 16px;
        position: relative;
    }
    .navbar .nav-item .nav-link {
        box-sizing: border-box;
        color: rgb(0, 0, 0);
        display: block;
        line-height: 23.4px;
        padding: 2px 0;
    }

    .nav-item.active::after, .nav-item:hover::after {
        background-color: #25d5d0;
        left: 0px;
        right: 0px;
    }
    .nav-item::after {
        content: " ";
        position: absolute;
        bottom: 0;
        left: 0px;
        right: 0px;
        height: 1px;
        transition: all .3s cubic-bezier(.42,.01,.58,1);
        z-index: 999999998;
        background-color: transparent;
    }
    .navbar .btn {
        font-size: 26px;
    }
    .navbar .btn:hover {
        color: rgb(0, 206, 200);
        border-color: transparent;
    }

    @include xs {
        .navbar {
            padding: 20px !important;
        }
    }

    @include md {
        .onScroll nav {
            padding: 0 20px 0 !important;
        }
        .navo {
            background-color: #fff;
            transform: translateY(20px);
        }
    }
    .navbar-toggler {
        border: 1px solid var(--main-color);
        outline: none;
        box-shadow: none !important;
    }
    .menu-trigger p {
        width: 30px;
        height: 5px;
        background: var(--main-color);
        margin: 0 0 2px;
    }
    .navbar .btn:hover {
        color: rgb(210, 52, 48);
        background-color: var(--main-color);
    }
    
    .side-bar {
        width: 0;
        position: fixed;
        overflow: hidden;
        top: 0;
        bottom: 0;
        right: 0;
        background-color: rgba(243, 245, 246, 0.95);
        z-index: 9999;
        transition: all .4s ease;
        padding: 0;
    }
    .side-bar.opend {
        width: 100%;
        background: rgba(0, 0, 0, 0.25);
    }
    .side-bar .content-wrapper {
        padding: 60px 30px;
        position: relative;
        overflow-x: hidden;
        overflow-y: auto;
        height: 100%;
        scrollbar-width: none;
        width: 300px;
        float: right;
        box-shadow: 0 0 5px 0 rgba(0,0,0,.15);
        background: #fff;
    }
    .side-bar .content-wrapper .close-btn {
        position: absolute;
        top: 20px;
        left: auto;
        right: 20px;
        color: rgb(97, 106, 125);
        font-size: 20px;
        cursor: pointer;
    }
    .side-bar .content-wrapper .widget {
        margin-bottom: 50px;
        
    }
    .side-bar .content-wrapper h4 {
        font-size: 18px;
        font-weight: 400;
        letter-spacing: 1px;
        line-height: 18px;
        margin-bottom: 28px;
        color: rgb(9, 41, 51)
    }
    .side-bar .content-wrapper p {
        color: rgb(166, 175, 179);
        font-size: 22px;
        font-weight: 400;
        line-height: 30.8px;
    }
    .side-bar .content-wrapper ul {
        list-style: none;
        padding: 0;     
    }
    .side-bar .content-wrapper ul li {
        color: rgb(97, 106, 125);
        align-items: start;
        display: flex;
    }
    .side-bar .content-wrapper ul li > div {
        display: inline-block;
    }
    .side-bar .content-wrapper ul li > div p {
        margin: -4px 0 0 12px;
    }
</style>