<template>
    <footer>
        <div class=" copyrights">
            <img src="https://the7.io/event-agency/wp-content/uploads/sites/48/2018/06/ev-f.png" alt="">
            <p> © Seven Business 2016-2017. All rights reserved.</p>
        </div>
    </footer>
</template>

<script>


export default {
    name: 'AppFooter',
    components: {},
    data() {
        return {
            
        }
    },
    beforeMount () {
        
    },
    methods : {
        
    }
}
</script>
<style>
    footer {
        background-color: #20262a;
    }
    footer .copyrights {
        padding: 20px 65px;
        text-align: center;

    }
    footer .copyrights p {
        color: rgb(255, 255, 255);
        font-size: 13px;
        font-weight: 400;
        line-height: 18.2px;
        text-align: center;
        margin: 15px 0 0;
    }
    footer h5 {
        color: rgb(255, 255, 255);
        font-size: 15px;
        line-height: 19.5px;
        margin-bottom: 20px;
    }
    footer h6 {
        color: rgb(255, 255, 255);
        font-size: 14px;
        line-height: 21px;
        margin-bottom: 5px;
        font-size: 14px;
        line-height: 21px;
        margin-bottom: 5px;
    }
    footer p {
        color: rgb(133, 134, 140);
        font-size: 14px;
        line-height: 21px;
    }
    footer .widgets a{
        background-color: rgba(133, 134, 140, 0.15);
        border-radius: 50%;
        color: rgb(133, 134, 140);
        font-size: 14px;
        height: 26px;
        line-height: 26px;
        margin-bottom: 2px;
        margin-left: 2px;
        margin-right: 2px;
        margin-top: 2px;
        position: relative;
        text-align: center;
        width: 26px;
        display: inline-block;
    }
</style>