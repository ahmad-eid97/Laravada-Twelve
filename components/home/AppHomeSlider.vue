<template>
    <section class="intro">
        <div class="row m-0 align-items-center">
            <div class="col-lg-6">
                    <h4>Advice for your unique business needs</h4>
                    <h6>
                        Achieve more for your business with us!
                    </h6>
                    <p>
                        Faucibus orci luctus - ut pharetra augue. Nullam non sapien quam. Nullam egestas, elit a viverra malesuada. Wondering ipsum dolor sit amet?
                    </p>
                    <a href="#" class="btn btn-primary">
                        Make an appointment
                    </a>
                    <a href="#" class="btn btn-alt">
                        Get free consultation 
                        <font-awesome-icon icon="fa-solid fa-arrow-right" />
                    </a>
            </div>
            <div class="col-lg-6 image">
                <img class="img-fluid"  src="https://the7.io/business-advisors/wp-content/uploads/sites/72/elementor/thumbs/art011-pds1a8pw55vosw0svd1ymgwfx0v59wcze4nxbvvq4w.jpg" alt="">
            </div>
        </div>
    </section>
</template>

<script>

export default {
    name: 'AppHomeSlider',
    data() {
        return {
            
        }
    },
    methods : {
        
    },
    mounted() {
        
    },
}
</script>
<style lang="scss">
    .intro {
        min-height: 100vh;
        position: relative;
        padding: 200px 60px 90px;
    }
    .intro h4{
        color: rgb(0, 206, 200);
        font-size: 26px;
        font-weight: 400;
        line-height: 33.8px;
        margin-bottom: 30px;
    }
    .intro h6 {
        color: rgb(0, 0, 0);
        font-size: 46px;
        font-weight: 400;
        line-height: 50.6px;
        margin-bottom: 30px;
        text-align: left;
    }

    @include sm {
        .intro {
            padding: 200px 20px 90px;
        }
        .intro h4{
            font-size: 20px;
            line-height: 33.8px;
        }
        .intro h6 {
            font-size: 30px;
            line-height: 40.6px;
        }
        img {
            width: 450px;
        }
    }

    @include xs {
        img {
            width: 300px;
        }
    }
    
    .intro p {
        color: rgb(94, 100, 107);
        font-size: 22px;
        line-height: 33px;
        margin-bottom: 40px;
    }
    .intro .btn {
        align-items: center;
        background-color: rgb(56, 71, 210);
        border-radius: 8px;
        border: none;
        box-shadow: rgba(0, 0, 0, 0) 0px 0px 10px 0px;
        color: rgb(255, 255, 255);
        font-size: 18px;
        font-weight: 400;
        justify-content: center;
        line-height: 18px;
        padding-bottom: 10px;
        padding-left: 26px;
        padding-right: 26px;
        padding-top: 10px;
        text-align: center;
        margin-right: 30px;
        margin-bottom: 20px;
        min-height: 56px;
        display: inline-flex;
    }
    .intro .btn-primary:hover {
        background-color: rgb(24, 37, 153);
    }
    .intro  .btn-alt {
        background-color: transparent;
        color: rgb(56, 71, 210);
        position: relative;
    }
    .intro  .btn-alt svg {
        margin-left: 5px;
        font-size: 14px;
    }
    .intro .btn-alt::after {
        content: "";
        position: absolute;
        left: 24px;
        right: 24px;
        height: 2px;
        background: #ced3ff;
        bottom: 12px;
    }
    .intro .btn-alt:hover {
        color: rgb(56, 71, 210);
    }
    .intro .btn-alt:hover::after {
        background: #9ea8fe;
    }
    .intro .image {
        position: relative;
    }
    .intro .image img {
        -webkit-mask-image: url(https://the7.io/business-advisors/wp-content/uploads/sites/72/2021/09/sqr012.svg);
        -webkit-mask-size: contain;
        -webkit-mask-position: center center;
        -webkit-mask-repeat: no-repeat;
        max-width: 580px;
    }
    .intro .image .image-icon {
        color: rgb(94, 100, 107);
        font-size: 18px;
        position: absolute;
        left: 390px;
        top: 345px;
        z-index: 3;
        width: 140px;
    }
</style>