<template>
    <div class="choose-area pt-100 pb-70">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6">
                    <div class="choose-content mr-20">
                        <div class="section-title">
                            <span class="sp-color1">Why Choose Us</span>
                            <h2>We Provide Truly Prominent It Solutions.</h2>
                            <p>
                            Aenean sollicitudin, lorem quis bibendum auctor, nisi elit consequat ipsum, nec sagittis sem nibh id elit. Duis sed odio sit amet nibh vulputate cursus a sit amet mauris. Morbi accumsan ipsum auctor a ornare odio.
                            </p>
                        </div>
                        <div class="row">
                            <div class="col-lg-6 col-6">
                                <div class="choose-content-card">
                                    <div class="content">
                                        <font-awesome-icon icon="fa-solid fa-hand-holding-hand" />
                                        <h3>Experience</h3>
                                    </div>
                                    <p>Neque porro quisquam est qui dolorem ipsum quia dolor sit amet</p>
                                </div>
                            </div>
                            <div class="col-lg-6 col-6">
                                <div class="choose-content-card">
                                    <div class="content">
                                        <font-awesome-icon icon="fa-solid fa-circle-question" />
                                        <h3>Quick Support</h3>
                                    </div>
                                    <p>Neque porro quisquam est qui dolorem ipsum quia dolor sit amet</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="choose-img">
                        <img src="/assets/images/choose-img.jpg" alt="Images">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppAboutChoose'
}
</script>

<style>
.choose-area {
    background-color: rgb(32, 43, 143);;
}
.choose-area .choose-content {
    margin-bottom: 30px;
    margin-right: 20px;
}
.choose-area .section-title {
  margin: 0 auto ;
  padding: 0;
  position: relative;
  text-align: start;
}
.choose-area .section-title span {
    color: rgb(0, 206, 200);
    font-size: 20px;
    font-weight: 400;
    line-height: 33.8px;
    margin-bottom: 10px;
}
.choose-content .section-title h2 {
    color: #fff;
    font-size: 40px;
    font-weight: 400;
    line-height: 50.6px;
    margin-bottom: 30px;
    text-align: left;
}
.choose-area .choose-content .section-title p {
    color: #fff;
    padding-top: 10px;
    margin-bottom: 0;
    max-width: 530px;
}
.choose-area .choose-content .choose-content-card {
    margin-top: 15px;
}
.choose-area .choose-content .choose-content-card .content {
    padding-top: 20px;
    position: relative;
    padding-left: 75px;
}
.choose-area .choose-content .choose-content-card .content svg {
    position: absolute;
    top: 10px;
    left: 0;
    font-size: 60px;
    color:#05cfc9;
    line-height: 1;
}
.choose-area .choose-content .choose-content-card .content h3 {
    margin-top: 10px;
    margin-bottom: 30px;
    font-weight: 800;
    color: #fff;
    font-size: 22px;
}
.choose-area .choose-content .choose-content-card p {
    margin-top: 5px;
    margin-bottom: 0;
    color: #fff;
}
.choose-area .choose-img {
    margin-bottom: 30px;
}
.choose-area .choose-img img {
  border-radius: 15px;
  -webkit-mask-image: url(https://the7.io/business-advisors/wp-content/uploads/sites/72/2021/09/sqr012.svg);
    -webkit-mask-size: contain;
    -webkit-mask-position: center center;
    -webkit-mask-repeat: no-repeat;
}
</style>