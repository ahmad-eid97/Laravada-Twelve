<template>
    <section class="contact">
        <div class="row m-0 align-items-center justify-content-center">
            <div class="col-lg-6 image">
                <img class="img-fluid"  src="https://the7.io/business-advisors/wp-content/uploads/sites/72/elementor/thumbs/art010-pds1596pvt1x7d9kzpg7w87egfg1fpk91g26o19x5c.jpg" alt="">
            </div>
            <div class="col-lg-6 textSide" style="padding: 0 60px;">
                <h3>
                    Let's figure out how we can improve your business!
                </h3>
                <p>
                    Wondering ipsum dolor sit amet? We consectetur adipiscing elit tempor incididunt ut labore.
                </p>
                <input type="text" class="form-control" placeholder="Name">
                <input type="text" class="form-control" placeholder="Phone number">
                <a href="#" class="btn btn-primary">
                    <font-awesome-icon icon="fa-solid fa-phone" />
                    Request a call-back
                </a>
                    
            </div>
        </div>
    </section>
</template>

<script>

export default {
    name: 'AppHomeContact',
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
    .contact {
        position: relative;
        padding: 0 0 90px;
    }
    .contact h3{
        color: rgb(0, 0, 0);
        font-size: 31px;
        font-weight: 400;
        line-height: 37.2px;
        margin-bottom: 30px;
    }
    
    .contact p {
        color: rgb(94, 100, 107);
        font-size: 18px;
        font-weight: 400;
        line-height: 28.8px;
        margin-bottom: 40px;
    }
    .contact .btn {
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
        display: flex;
    }
    .contact .btn-primary:hover {
        background-color: rgb(24, 37, 153);
    }
    
    .contact  .btn svg {
        margin-right: 12px;
    }
    .contact .btn-alt::after {
        content: "";
        position: absolute;
        left: 24px;
        right: 24px;
        height: 2px;
        background: #ced3ff;
        bottom: 12px;
    }
    .contact .btn-alt:hover {
        color: rgb(56, 71, 210);
    }
    .contact .btn-alt:hover::after {
        background: #9ea8fe;
    }
    .contact .image {
        position: relative;
        display: flex;
        justify-content: center;
    }
    .contact .image img {
        -webkit-mask-image: url(https://the7.io/business-advisors/wp-content/uploads/sites/72/2021/09/sqr009.svg);
        -webkit-mask-size: contain;
        -webkit-mask-position: center center;
        -webkit-mask-repeat: no-repeat;
        max-width: 580px;
    }
    .contact .image .image-icon {
        color: rgb(94, 100, 107);
        font-size: 18px;
        position: absolute;
        left: 390px;
        top: 345px;
        z-index: 3;
        width: 140px;
    }
    .contact .form-control {
        background-color: rgb(255, 255, 255);
        border:2px solid rgb(226, 233, 239);
        border-radius: 6px;
        color: rgb(0, 0, 0);
        font-size: 18px;
        height: 59px;
        line-height: 26px;
        max-width: 100%;
        min-height: 59px;
        padding-bottom: 7px;
        padding-left: 20px;
        padding-right: 20px;
        padding-top: 7px;
        margin-bottom: 20px;
    }
    @include xs {
        .textSide {
            padding: 20px !important;
        }
    }
</style>