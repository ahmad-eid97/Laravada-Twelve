<template>
  <header
    :class="!topOfPage ? 'onScroll' : ''"
    class="header header-style-2 clearfix"
  >
    <div class="cart" :class="openCart ? 'opened' : ''">
      <div class="head">
        <i class="fa-regular fa-xmark" @click="openCart = false"></i>
        <button
          @click="goToCheckout"
          :disabled="$store.state.cartItems.length <= 0"
        >
          <i class="fa-regular fa-badge-check"></i> Checkout
        </button>
      </div>
      <cart />
    </div>
    <div class="row m-0 w-100">
      <app-top-bar class="col-12"></app-top-bar>
      <b-navbar toggleable="lg">
        <b-navbar-brand :href="localePath('/')">
          <img src="/assets/images/logo.png" alt="logoImage" />
        </b-navbar-brand>

        <div class="d-flex align-items-center smallScr">
          <div class="m-0 cartIcon" @click="openCart = !openCart">
            <span>{{ $store.state.cartItems.length }}</span>
            <i class="fa-regular fa-cart-plus"></i>
          </div>
          <b-navbar-toggle target="navbar-toggle-collapse">
            <template #default="{ expanded }">
              <span
                class="menu-trigger"
                :class="expanded ? 'active' : ''"
                id="menu03"
              >
                <p></p>
                <p></p>
                <p></p>
              </span>
            </template>
          </b-navbar-toggle>
          <div v-if="$store.state.user" class="logout" @click="logout">
            <i class="fa-regular fa-right-from-bracket"></i>
          </div>
        </div>
        <b-collapse
          id="navbar-toggle-collapse"
          class="ml-auto justify-content-end navo"
          is-nav
        >
          <b-navbar-nav class="align-items-center">
            <b-nav-item :to="localePath('/')">Home</b-nav-item>
            <b-nav-item :to="localePath('/about')">About</b-nav-item>
            <b-nav-item :to="localePath('/team')">Team</b-nav-item>
            <b-nav-item :to="localePath('/services')">Services</b-nav-item>
            <b-nav-item :to="localePath('/testimonials')">Projects</b-nav-item>
            <b-nav-item :to="localePath('/blogs')">News</b-nav-item>
            <b-nav-item :to="localePath('/careers')">Career</b-nav-item>
            <b-nav-item :to="localePath('/events')">Events</b-nav-item>
            <b-nav-item :to="localePath('/contact')">Contact</b-nav-item>
            <b-nav-item
              :to="localePath('/login')"
              v-if="$store.state.user"
              class="outLarge"
              @click="logout"
              >Logout</b-nav-item
            >
          </b-navbar-nav>
        </b-collapse>

        <div class="d-flex align-items-center largeScr">
          <div class="m-0 cartIcon" @click="openCart = !openCart">
            <span>{{ $store.state.cartItems.length }}</span>
            <i class="fa-regular fa-cart-plus"></i>
          </div>
          <div v-if="$store.state.user" class="logout" @click="logout">
            <i class="fa-regular fa-right-from-bracket"></i>
          </div>
        </div>
      </b-navbar>
      <div
        :class="side ? 'opend' : ''"
        @click.self="side = !side"
        class="side-bar"
      >
        <div class="content-wrapper">
          <div class="close-btn">
            <i class="fa-solid fa-xmark" @click="side = !side"></i>
          </div>
          <div class="widge">
            <p>No products in the cart.</p>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import cart from "../cart/cart.vue";
import AppTopBar from "./AppTopBar.vue";
export default {
  name: "AppHeader",
  components: {
    AppTopBar,
    cart,
  },
  data() {
    return {
      side: false,
      topOfPage: true,
      openCart: false,
    };
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  mounted() {},
  methods: {
    logout() {
      this.$store.commit("setUserData", null);
      this.$cookies.remove("cms-auth");
      this.$cookies.remove("cms-user");
      this.$router.push(this.localePath("/login"));
    },
    handleScroll() {
      if (window.pageYOffset > 30) {
        if (this.topOfPage) this.topOfPage = false;
      } else {
        if (!this.topOfPage) this.topOfPage = true;
      }
    },
    goToCheckout() {
      this.openCart = false;
      this.$router.push("/checkout");
    },
  },
};
</script>
<style lang="scss">
header {
  position: fixed;
  left: 0;
  right: 0;
  z-index: 10;
  background: transparent;
  .cart {
    width: 390px;
    height: 100vh;
    position: fixed;
    top: 0;
    right: 0;
    transform: translateX(390px);
    background-color: #fff;
    z-index: 999999;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.2);
    .head {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 10px;
      & > i {
        border: 1px solid var(--main-color);
        border-radius: 5px;
        width: 30px;
        height: 30px;
        display: grid;
        place-items: center;
        cursor: pointer;
        background-color: var(--main-color);
        color: #fff;
        &:hover {
          color: var(--main-color);
          background: transparent;
        }
      }
      button {
        padding: 5px 30px;
        font-size: 1.1rem;
        background-color: var(--main-color);
        color: #fff;
        border: 1px solid var(--main-color);
        display: flex;
        align-items: center;
        gap: 5px;
        i {
          font-size: 1.1rem;
        }
        &:disabled {
          opacity: 0.5;
          cursor: not-allowed;
          &:hover {
            background-color: var(--main-color);
            color: #fff;
          }
        }
        &:hover {
          background-color: transparent;
          color: var(--main-color);
        }
      }
    }
    &.opened {
      transform: translateX(0);
    }
    @include xs {
      width: 350px;
    }
  }
  .cartIcon {
    border: 1px solid var(--main-color);
    border-radius: 5px;
    width: 45px;
    height: 45px;
    display: grid;
    place-items: center;
    cursor: pointer;
    position: relative;
    margin: 0 15px !important;
    span {
      position: absolute;
      top: -15px;
      right: -10px;
      width: 30px;
      height: 30px;
      background-color: var(--main-color);
      border-radius: 50%;
      color: #fff;
      display: grid;
      place-content: center;
      font-size: 1.2rem;
      @include sm {
        font-size: 1rem;
      }
    }
    i {
      color: var(--main-color);
    }
    @include sm {
      width: 40px;
      height: 40px;
      margin: 0 10px !important;
    }
    &:hover {
      background-color: var(--main-color);
      border-color: var(--main-color);
      i {
        color: #fff;
      }
    }
  }
}
.logout {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: var(--main-color);
  color: #fff;
  display: grid;
  place-items: center;
  font-size: 1.2rem;
  cursor: pointer;
  @include md {
    display: none;
  }
}
.outLarge {
  display: none;
  @include md {
    display: inline;
  }
}
.smallScr {
  align-items: center;
  display: none !important;
  @include md {
    display: flex !important;
  }
}
.largeScr {
  align-items: center;
  display: flex !important;
  @include md {
    display: none !important;
  }
}
.onScroll {
  position: fixed;
  width: 100%;
  padding: 20px 0;
  // height: 70px;
  display: flex;
  align-items: center;
  transition: all 0.2s ease-in-out;
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

.nav-item.active::after,
.nav-item:hover::after {
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
  transition: all 0.3s cubic-bezier(0.42, 0.01, 0.58, 1);
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
  margin: 0;
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
  transition: all 0.4s ease;
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
  box-shadow: 0 0 5px 0 rgba(0, 0, 0, 0.15);
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
  color: rgb(9, 41, 51);
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
