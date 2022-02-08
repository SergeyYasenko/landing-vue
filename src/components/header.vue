<template >
   <div class="header">
      <div class="header__container container">
         <div class="header__row">
            <div class="header__logo">
               <transition class="header__burger-line" name="fade" mode="out-in">
                  <i class="material-icons menu" v-if="!show" @click="show = !show" key="menu">menu</i>
                  <i class="material-icons close" v-else @click="show = !show" key="close">close</i>
               </transition>
               <nav class="header__burger-menu">
                  <transition name="fade">
                     <ul v-if="show">
                        <li
                        v-for="item in items"
                        :key="item.id"
                        class="header__menu-item"
                        > {{ item }} </li>
                     </ul>
                  </transition>
               </nav>
               <h1 class="header__logo-title" >{{message}}</h1>
            </div>
            <ul class="header__contact-list">
               <li class="header__contact-link"><a href="#"><img src="../assets/image/icons/facebook.svg" alt="facebook"></a></li>
               <li class="header__contact-link"><a href="#"><img src="../assets/image/icons/twitter.svg" alt="twitter"></a></li>
               <li class="header__contact-link"><a href="#"><img src="../assets/image/icons/instagram.svg" alt="instagram"></a></li>
            </ul>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   name: 'Header',
   data: function () {
      return {
         message: 'ARCH',
         items: [
            'Home',
            'About',
            'Blog',
            'Map',
            'Contacts',
         ],
         show: false,
      }
   }
};



</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

@import url("https://fonts.googleapis.com/icon?family=Material+Icons");

.header {
   width: 100%;
   padding: 16px 0;
   background-color:#F7F2E2;
}

.header__row {
   display: flex;
   justify-content: space-between;
}

.header__logo {
   display: flex;
}

.material-icons {
   width: 48px;
   height: 48px;
   background-color: #fff;
   color: #DD514C;
   border-radius: 50%;
   margin-right: 16px;
   display: flex;
   align-items: center;
   justify-content: center;
}

.header__burger-line span:last-child {
   margin: 0;
}

.fade-enter-active,
.fade-leave-active {
   transition: opacity .3s ease;
}

.fade-enter,
.fade-leave-to {
   opacity: 0;
}

.menu,
.close {
   cursor: pointer;
   transition: all .3s ease;
}

.header__burger-menu {
   background-color: #fff;
   position: absolute;
   top: 0;
   left: 0;
   min-width: 300px;
}

.header__menu-item {
   width: 100%;
   text-align: center;
   padding: 20px 0;
}

.header__menu-item:first-child {
   padding-top: 40px;
}


.header__logo-title {
   font-weight: bold;
   font-size: 40px;
   line-height: 48px;
}

.header__contact-list {
   display: flex;
}

.header__contact-link {
   width: 48px;
   height: 48px;
   background-color: #fff;
   border-radius: 50%;
   margin-right: 8px;
   display: flex;
   align-items: center;
   justify-content: center;
}

.header__contact-link:last-child {
   margin: 0;
}


</style>
