<template >
   <div class="header">
      <div class="header__container container">
         <div class="header__row">
            <div class="header__logo">
               <div class="header__burger-line">
                  <span></span>
                  <span></span>
                  <span></span>
               </div>
               <div class="header__burger-menu">
                  <ul class="header__menu-list">
                     <li class="header__menu-link"><a href="#">home</a></li>
                     <li class="header__menu-link"><a href="#">About Us</a></li>
                     <li class="header__menu-link"><a href="#">Contacts</a></li>
                  </ul>
               </div>
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
         message: 'ARCH'
      }
   },
}



</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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

.header__burger-line {
   width: 48px;
   height: 48px;
   background-color: #fff;
   border-radius: 50%;
   margin-right: 16px;
   display: flex;
   flex-direction: column;
   align-items: center;
   justify-content: center;
}

.header__burger-line span {
   width: 12px;
   height: 2px;
   background-color: #DD514C;
   display: block;
   margin-bottom: 5px;
}

.header__burger-line span:last-child {
   margin: 0;
}

.header__burger-menu {}

.header__menu-list {
   display: none;
}

.header__menu-link {}


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

.header__menu-link:last-child {
   margin: 0;
}


</style>
