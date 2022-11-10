<template>
  <section class="cases">
        <div class="row m-0">
            <h2>
                Featured case studies
            </h2>
        </div>
        <div class="row m-0">

            <swiper :options="swiperOption">
                <swiper-slide>
                <div>
                    <div class="item">
                        <img src="https://the7.io/business-advisors/wp-content/uploads/sites/72/2020/04/l0-2-768x384.png" alt="">
                        <h4 class="">
                            New strategy implementation
                        </h4>
                        
                        <div class="row">

                            <a href="#" class="btn col-auto">
                                Learn more
                            </a>

                        </div>
                    </div>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div>
                    <div class="item">
                    <img src="https://the7.io/business-advisors/wp-content/uploads/sites/72/2020/04/l0-3-768x384.png" alt="">
                    <h4 class="">
                        Successful international product launch
                    </h4>
                    
                    <div class="row">

                        <a href="#" class="btn col-auto">
                            Learn more
                        </a>

                    </div>
                    </div>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div>
                    <div class="item">
                        <img src="https://the7.io/business-advisors/wp-content/uploads/sites/72/2020/04/l0-4-768x384.png" alt="">
                        <h4 class="">
                            Full business reorganisation in 30 days
                        </h4>
                        
                        <div class="row">

                            <a href="#" class="btn col-auto">
                                Learn more
                            </a>

                        </div>
                    </div>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div>
                    <div class="item">
                        <img src="https://the7.io/business-advisors/wp-content/uploads/sites/72/2020/04/llgg000-768x384.png" alt="">
                        <h4 class="">
                            150% more returning customers
                        </h4>
                        
                        <div class="row">

                            <a href="#" class="btn col-auto">
                                Learn more
                            </a>

                        </div>
                    </div>
                </div>
                </swiper-slide>
            </swiper>

        </div>
  </section>
</template>

<script>
export default {
    name: 'AppHomeCases',
    data () {
        return {
        swiperOption: {
            loop: true,
            slidesPerView: 3,
            spaceBetween: 50,
            breakpoints: {
            // when window width is >= 320px
            100: {
                slidesPerView: 1,
                spaceBetween: 5,
            },
            // when window width is >= 480px
            480: {
                slidesPerView: 1,
                spaceBetween: 5,
            },
            // when window width is >= 640px
            640: {
                slidesPerView: 1,
                spaceBetween: 5,
            },
            992: {
                slidesPerView: 2,
                spaceBetween: 5,
            },
            1200: {
                slidesPerView: 3,
                spaceBetween: 5,
            },
            },
        },
        }
        
    }
}
</script>

<style lang="scss">
    .cases {
        margin: 0 0 60px;
        padding: 30px 60px;
    }
    @include xs {
        .cases {
            padding: 30px 20px;
        }
    }
    .cases h2 {
        color: rgb(0, 0, 0);
        font-size: 38px;
        font-weight: 400;
        line-height: 45.6px;
        margin-bottom: 60px;
        text-align: center;
    }
    .cases .item {
        align-content: center;
        align-items: center;
        border-radius: 8px;
        border: 2px solid #e2e9ef;
        display: block;
        flex-direction: row;
        flex-wrap: nowrap;
        font-size: 18px;
        height: 400px;
        margin: 0 15px 30px;
        min-height: 400px;
        padding-bottom: 45px;
        padding-left: 30px;
        padding-right: 30px;
        padding-top: 45px;
        justify-content: center;
    }
    .cases .item img {
        margin: 0 auto 40px;
        width: 260px;
    }
    .cases .item h4 {
        color: rgb(0, 0, 0);
        font-size: 25px;
        font-weight: 400;
        line-height: 33.8px;
        text-align: center;
    }
    .cases .item p {
        color: rgb(94, 100, 107);
        font-size: 18px;
        font-weight: 400;
        line-height: 28.8px;
        margin-top: 20px;
        text-align: center;
    }
    .cases .item span {
        color: rgb(0, 206, 200);
        font-size: 18px;
        font-weight: 400;
        line-height: 28.8px;
        text-align: center;
    }
    .cases .item .btn {
        align-items: center;
        background-color: rgb(63, 82, 254);
        border-radius: 6px;
        border: none;
        box-shadow: rgba(0, 0, 0, 0) 0px 0px 10px 0px;
        color: rgb(255, 255, 255);
        display: flex;
        font-size: 14px;
        font-weight: 400;
        line-height: 14px;
        margin: 30px auto 0;
        min-height: 36px;
        min-width: 50px;
        padding-bottom: 8px;
        padding-left: 14px;
        padding-right: 14px;
        padding-top: 8px;
        text-align: center;
        text-decoration-color: rgb(255, 255, 255);
        text-decoration-line: none;
        text-decoration-style: solid;
        text-decoration-thickness: auto;
        transition-delay: 0s;
        transition-duration: 0.3s;
        transition-property: all;
        transition-timing-function: ease;
        display: inline-block;
    }
    .cases .slick-slide > div {
        text-align: center;
    }
    .cases .slick-prev {
        left: -25px;
    }
    .cases .slick-next {
        right: -25px;
    }
    .cases .slick-prev, .cases .slick-next {
        width: 40px;
        height: 40px;
        z-index: 2;
    }
    .cases .slick-prev::before, .cases .slick-next::before {
        font-family: 'slick';
        font-size: 40px;
        line-height: 1;
        opacity: 0.75;
        color: #a7afb3;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }
</style>
