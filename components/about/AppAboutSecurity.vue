<template>
    <div class="security-area pt-100 pb-70">
        <div class="container">
            <div class="section-title text-center">
                <span class="sp-color2">IT Security &amp; Computing</span>
                <h2>Searching for a Solution! We Provide Truly Prominent IT Solutions</h2>
                
            </div>
            <div class="row pt-45">
                <div class="col-lg-4 col-sm-6">
                <div class="security-card">
                    <div class="icon">
                        <font-awesome-icon icon="fa-solid fa-building-lock" />
                    </div>
                    <h3>
                        <a href="#">Business Security</a>
                    </h3>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam blandit scelerisque ullamcorper proin scelerisque tortor odio.</p>
                </div>
                </div>
                <div class="col-lg-4 col-sm-6">
                    <div class="security-card">
                        <div class="icon">
                            <font-awesome-icon icon="fa-solid fa-computer" />
                        </div>
                        <h3>
                            <a href="#">Manage IT Service</a>
                        </h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam blandit scelerisque ullamcorper proin scelerisque tortor odio.</p>
                    </div>
                </div>
                <div class="col-lg-4 col-sm-6">
                    <div class="security-card">
                        <div class="icon">
                            <font-awesome-icon icon="fa-solid fa-magnifying-glass-chart" />
                        </div>
                        <h3>
                            <a href="#">Product Analysis</a>
                        </h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam blandit scelerisque ullamcorper proin scelerisque tortor odio.</p>
                    </div>
                </div>
                <div class="col-lg-4 col-sm-6">
                    <div class="security-card">
                        <div class="icon">
                            <font-awesome-icon icon="fa-solid fa-file-circle-check" />
                        </div>
                        <h3>
                            <a href="case-details.html">Analytic Solution</a>
                        </h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam blandit scelerisque ullamcorper proin scelerisque tortor odio.</p>
                    </div>
                </div>
                <div class="col-lg-4 col-sm-6">
                    <div class="security-card">
                        <div class="icon">
                            <font-awesome-icon icon="fa-solid fa-award" />
                        </div>
                        <h3>
                            <a href="case-details.html">Finest Quality</a>
                        </h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam blandit scelerisque ullamcorper proin scelerisque tortor odio.</p>
                    </div>
                </div>
                <div class="col-lg-4 col-sm-6">
                    <div class="security-card">
                        <div class="icon">
                            <font-awesome-icon icon="fa-solid fa-cubes" />
                        </div>
                        <h3>
                            <a href="case-details.html">Risk Management</a>
                        </h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam blandit scelerisque ullamcorper proin scelerisque tortor odio.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
.section-title {
    margin: 0 auto;
    padding: 0;
    position: relative;
    text-align: center;
}
.security-area .section-title span {
    color: rgb(0, 206, 200);
    font-size: 20px;
    font-weight: 400;
    line-height: 33.8px;
    margin-bottom: 10px;
}
.security-area .section-title h2 {
    color: #000;
    font-size: 40px;
    font-weight: 400;
    line-height: 50.6px;
    margin-bottom: 30px;
    text-align: center;
}
.security-area .seprator img {
  width: 70px;
  margin-top: 5px;
  margin-bottom: 20px;
}
.security-card {
    padding: 40px 30px 35px;
    border-radius: 8px;
    border: 2px solid #e2e9ef;
    position: relative;
    z-index: 1;
    margin-bottom: 30px;
    color: #212934;
}
.security-card h3 a {
    color: #212934;
}
.security-card:hover h3 a,
.security-card:hover p {
    color: #fff;
}
.security-card::before {
    content: '';
    position: absolute;
    z-index: -1;
    bottom: 0;
    right: 0;
    width: 90px;
    height: 90px;
    background-color:#05cfc9;
    border-radius: 272px 0 180px;
    opacity: .1;
    -webkit-transition: .7s;
    transition: .7s;
}

.security-card::after {

    content: '';
    position: absolute;
    z-index: -1;
    bottom: 0;
    right: 0;
    width: 75px;
    height: 75px;
    background-color:#05cfc9;
    border-radius: 170px 0 136px;
    opacity: .1;
    -webkit-transition: .7s;
    transition: .7s;
}
.security-card:hover::before {
    width: 100%;
    height: 100%;
    border-radius: 60px 8px;
    opacity: 1;
}
.security-card .icon {
    font-size: 45px;
    width: 80px;
    height: 80px;
    line-height: 80px;
    color: #fff;
    background-color:#05cfc9;
    border-radius: 30px 8px;
    display: inline-block;
    text-align: center;
    margin-bottom: 12px;
    -webkit-transition: .5s;
    transition: .5s;
}
.security-card:hover .icon {
    font-size: 45px;
    width: 80px;
    height: 80px;
    line-height: 80px;
    color: #05cfc9;
    background-color: #fff;
    border-radius: 30px 8px;
    display: inline-block;
    text-align: center;
    margin-bottom: 12px;
    -webkit-transition: .5s;
    transition: .5s;
}
</style>