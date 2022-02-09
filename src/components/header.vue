<template >
  <div class="header">
    <div class="header__container container">
      <div class="header__row">
        <div class="header__menu">
          <i
            class="material-icons menu"
            @click="toggleClass(0)"
            v-bind:class="{ option_box: true, open: isOpen(0) }"
            key="menu"
            >menu</i
          >
          <nav
            v-bind:class="{ option_box: true, open: isOpen(0) }"
            class="header__burger-menu"
          >
            <i
              class="material-icons close"
              @click="toggleClass(0)"
              v-bind:class="{ option_box: true, open: isOpen(0) }"
              key="close"
              >close</i
            >
            <ul>
              <li class="header__menu-item">
                <a
                  v-for="item in items"
                  :key="item.title"
                  :href="item.path"
                  target="_blank"
                >
                  {{ item.title }}
                </a>
              </li>
              <div class="header__contact-list-m">
                <li class="header__contact-item-m">
                  <a href="#" target="_blank"
                    ><img
                      src="../assets/image/icons/facebook.svg"
                      alt="facebook"
                  /></a>
                </li>
                <li class="header__contact-item-m">
                  <a href="#" target="_blank"
                    ><img src="../assets/image/icons/twitter.svg" alt="twitter"
                  /></a>
                </li>
                <li class="header__contact-item-m">
                  <a href="#" target="_blank"
                    ><img
                      src="../assets/image/icons/instagram.svg"
                      alt="instagram"
                  /></a>
                </li>
              </div>
            </ul>
          </nav>
          <h1 class="header__logo-title">
            {{ message }}
          </h1>
        </div>
        <ul class="header__contact-list">
          <li class="header__contact-item">
            <a href="#" target="_blank"
              ><img src="../assets/image/icons/facebook.svg" alt="facebook"
            /></a>
          </li>
          <li class="header__contact-item">
            <a href="#" target="_blank"
              ><img src="../assets/image/icons/twitter.svg" alt="twitter"
            /></a>
          </li>
          <li class="header__contact-item">
            <a href="#" target="_blank"
              ><img src="../assets/image/icons/instagram.svg" alt="instagram"
            /></a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data: function () {
    return {
      message: "ARCH",
      items: [
        { title: "Home", path: "#" },
        { title: "About", path: "#" },
        { title: "Contact", path: "#" },
        { title: "Work With Us", path: "#" },
        { title: "Logout", path: "#" },
      ],
      openData: [{ isOpen: false }, { isOpen: false }, { isOpen: false }],
      close: false,
    };
  },
  methods: {
    toggleClass(i) {
      this.openData[i].isOpen = !this.openData[i].isOpen;
    },
    isOpen(i) {
      return this.openData[i].isOpen;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url("https://fonts.googleapis.com/icon?family=Material+Icons");

.header {
  width: 100%;
  padding: 16px 0;
  background-color: #f7f2e2;
}

.header__row {
  display: flex;
  justify-content: space-between;
}

.header__menu {
  display: flex;
}

.material-icons {
  width: 48px;
  height: 48px;
  background-color: #fff;
  color: #dd514c;
  border-radius: 50%;
  margin-right: 16px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
}

.header__burger-line span:last-child {
  margin: 0;
}

.menu {
  cursor: pointer;
}

.menu.open {
  opacity: 0;
  pointer-events: none;
  transition: all 0.3s ease;
}

.close {
  position: absolute;
  left: 30px;
  top: 15px;
  z-index: 4;
  cursor: pointer;
  background-color: #f7f2e2;
}

.header__burger-menu {
  background-color: #fff;
  position: absolute;
  top: 0;
  left: -100%;
  min-width: 300px;
  height: 100vh;
  z-index: 3;
  transition: all 0.3s ease;
  padding-top: 60px;
}

.header__burger-menu.open {
  left: 0;
  transition: all 0.3s ease;
}

.header__menu-item a {
  color: #333;
  display: block;
  width: 100%;
  text-align: center;
  padding: 20px 0;
  text-decoration: none;
}

.header__logo-title {
  font-weight: bold;
  font-size: 40px;
  line-height: 48px;
}

.header__contact-list,
.header__contact-list-m {
  display: flex;
}

.header__contact-list-m {
  width: 100%;
  justify-content: center;
  align-items: center;
}

.header__contact-item a,
.header__contact-item-m a {
  width: 48px;
  height: 48px;
  background-color: #fff;
  border-radius: 50%;
  margin-right: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.header__contact-item-m a {
  background-color: #f7f2e2;
  margin-top: 30px;
}

.header__contact-item:last-child,
.header__contact-item-m:last-child {
  margin: 0;
}

@media screen and (max-width: 576px) {
  .header__contact-list {
    display: none;
  }
}
</style>
