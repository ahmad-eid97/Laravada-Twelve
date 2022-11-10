<template>
    <section class="why">
        <div class="row m-0 align-items-center justify-content-center">
            <div class="col-lg-6" style="padding: 0 60px;">
                    <h3>
                        Why work with us
                    </h3>
                    <p>
                        We consectetur adipiscing elit tempor incididunt ut labore. Wondering ipsum dolor sit amet? We consectetur adipiscing ipsum nulla glavrida elit tempor incididunt.
                    </p>
                    <ul>
                        <li>
                            <font-awesome-icon icon="fa-solid fa-check" />
                            Duis aute irure dolor in ipsum
                        </li>
                        <li>
                            <font-awesome-icon icon="fa-solid fa-check" />
                            Lopsum in lorem ipsum amet dolor glavrida
                        </li>
                        <li>
                            <font-awesome-icon icon="fa-solid fa-check" />
                            In det nulla amet glavridsa reprehend
                        </li>
                        <li>
                            <font-awesome-icon icon="fa-solid fa-check" />
                            Sit lorem ipsum dolor sit amet glavrida
                        </li>
                        <li>
                            <font-awesome-icon icon="fa-solid fa-check" />
                            Lorem ipsum in lorem ipsum amet dolor glavrida
                        </li>
                    </ul>
            </div>
            <div class="col-lg-6 image">
                <img class="img-fluid"  src="https://the7.io/business-advisors/wp-content/uploads/sites/72/elementor/thumbs/art008-pdrzl0icyo2ajayjee9tpf4iwgnevoafb2uay0nxg0.jpg" alt="">
            </div>
        </div>
    </section>
</template>

<script>

export default {
    name: 'AppHomeWhy',
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
<style>
    .why {
        position: relative;
        padding: 0 0 90px;
    }
    .why h3{
        color: rgb(0, 0, 0);
        font-size: 31px;
        font-weight: 400;
        line-height: 37.2px;
        margin-bottom: 30px;
    }
    
    .why p {
        color: rgb(94, 100, 107);
        font-size: 18px;
        font-weight: 400;
        line-height: 28.8px;
        margin-bottom: 40px;
    }
    .why ul {
        list-style: none;
        padding: 0;
    }
    .why li {
        color: rgb(0, 0, 0);
        font-size: 18px;
        margin: 7.5px 0 0;
        padding: 0 0 7.5px;
    }
    .why li svg{
        color: rgb(0, 206, 200);
        font-size: 20px;
        margin-right: 5px;
    }
    .why .image {
        position: relative;
        display: flex;
        flex-direction: columns;
        justify-content: center;
    }
    .why .image img {
        -webkit-mask-image: url(https://the7.io/business-advisors/wp-content/uploads/sites/72/2021/09/sqr005.svg);
        -webkit-mask-size: contain;
        -webkit-mask-position: center center;
        -webkit-mask-repeat: no-repeat;
        max-width: 580px;
    }
    .why .image .image-icon {
        color: rgb(94, 100, 107);
        font-size: 18px;
        position: absolute;
        left: 390px;
        top: 345px;
        z-index: 3;
        width: 140px;
    }
    .why .form-control {
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
</style>