<template>
    <header :class="!topOfPage ? 'onScroll' : ''" class="header header-style-2 clearfix">
        <div class="row m-0 w-100">
            <b-navbar toggleable="lg">
                <b-navbar-brand href="#">
                    <img src="https://the7.io/event-agency/wp-content/uploads/sites/48/2018/06/l-event-7.png" alt="">
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

                <b-collapse id="navbar-toggle-collapse" class="ml-auto justify-content-between" is-nav>
                    <b-navbar-nav class="align-items-center">
                        <b-nav-item to="/">Home</b-nav-item>
                        <b-nav-item to="/about">About</b-nav-item>
                        <b-nav-item to="/services">Services</b-nav-item>
                        <b-nav-item to="/testimonials">Testimonials</b-nav-item>
                        <b-nav-item to="/blogs">News</b-nav-item>
                        <b-nav-item to="/contact">Contact</b-nav-item>
                    </b-navbar-nav>
                    <a href="#"  class="btn">
                        REQUEST A QUOTE
                        <font-awesome-icon icon="fa-solid fa-angle-right" />
                    </a>
                </b-collapse>
            </b-navbar>
        </div>
    </header>
</template>

<script>

export default {
    name: 'AppHeader',
    data() {
        return {
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
        top: 0;
        left: 0;
        right: 0;
        z-index: 10;
        background-color: rgb(234, 54, 46);
        position: fixed;
    }
    
    nav {
        padding: 0 60px 0 !important;
    }
    .onScroll nav {
        padding: 0 60px 0 !important;
    }
    .onScroll nav .nav-item {
        padding: 20px 10px;
    }
    .navbar-brand {
        width: 180px;
        transition: all 0.3s linear;
    }
    .navbar-brand img{
        max-width: 100%;
        transition: all 0.3s linear;
    }
    .onScroll .navbar-brand img{
        max-width: 70px;
    }
    
    .navbar .nav-item {
        margin: 0 1px;
        position: relative;
        padding: 34px 10px;
        transition: all 0.3s linear;
    }
    .navbar .nav-item.active, .navbar .nav-item:hover {
        background-color: rgba(0, 0, 0, 0.09);
    }
    .navbar .nav-item .nav-link {
        color: rgb(255, 255, 255);
        font-size: 18px;
        font-weight: 400;
        line-height: 22px;
    }

    
    .navbar .btn {
        background-color: rgb(210, 52, 48);
        border-radius: 500px;
        color: rgb(255, 255, 255);
        font-size: 14px;
        font-weight: 500;
        line-height: 18px;
        padding-bottom: 12px;
        padding-left: 22px;
        padding-right: 20px;
        padding-top: 12px;
    }
    .navbar-toggler {
        border: 1px solid #fff;
        outline: none;
        box-shadow: none !important;
    }
    .menu-trigger p {
        width: 30px;
        height: 5px;
        background: #fff;
        margin: 0 0 2px;
    }
    .navbar .btn:hover {
        color: rgb(210, 52, 48);
        background-color: rgb(255, 255, 255);
    }
    @include md {
        .onScroll .navbar-nav {
            transform: translateY(-10px);
        }
        .navbar-nav {
            padding: 20px 0;
            transform: translateY(-10px);
        }
        .navbar-nav li {
            padding: 5px 0 !important;
        }
        .navbar-nav li.nav-item a {
            color: #fff !important;
            padding: 5px 20px;
        }
        .btn {
            display: none;
        }
    }
    
    
</style>