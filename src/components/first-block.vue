<template>
   <div class="offer container">
      <div class="offer__row">
         <div class="offer__content">
            <div class="offer__sub-title">Architect for You</div>
            <div class="offer__title">
               We Develop <br />
               Great Designs
            </div>
            <a href="#" class="offer__btn">Contact us</a>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   name: "Main",
};
</script>

<style>
.offer {
   background-image: url("/src/assets/image/blocks/bg-image.png");
   background-position: 0 0;
   background-repeat: no-repeat;
   background-size: 100%;
}

.offer__row {
   display: flex;
   flex-direction: column;
   justify-content: center;
   height: 100vh;
}

.offer__content {
}

.offer__sub-title {
   font-weight: 700;
   font-size: 18px;
   line-height: 32px;
   padding-bottom: 21px;
}

.offer__title {
   font-weight: bold;
   font-size: 72px;
   line-height: 111%;
   padding-bottom: 33px;
}

.offer__btn {
   background: #dd514c;
   border-radius: 24px;
   font-weight: bold;
   font-size: 18px;
   line-height: 28px;
   color: #fff;
   text-decoration: none;
   padding: 10px 34px;
   display: inline-block;
}
</style>
