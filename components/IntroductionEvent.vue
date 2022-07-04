<template>
    <div class="row align-items-md-stretch">
      <div class="col-md-6">
        <div class="h-100 p-5">
          <img loding="lazy" width="499" height="387" src="~/assets/img/Introduction.svg" title="معرفی و توضیح مسابقه" alt="معرفی و توضیح مسابقه">
        </div>
      </div>
      <div class="col-md-6">
        <div class="h-100 p-5 text-right Introduction-box">
          <h2 class="mb-4"> معرفی و توضیح مسابقه</h2>
          <p v-if="show===false">لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده از طراحان گرافیک است، چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است، و برای شرایط فعلی تکنولوژی مورد نیاز، و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشدلورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده از طراحان گرافیک است، چاپگرها و متون بلکه روزنامه و مجله در</p>
            <video class="mb-4" width="100%" height="240" controls v-else style="border-radius: 10px">
              <source src="movie.mp4" type="video/mp4">
              <source src="movie.ogg" type="video/ogg">
              Your browser does not support the video tag.
            </video>
          <button class="btn btn-outline-light show-btn" type="button"  v-on:click="show = !show">
            <img loding="lazy" width="36" height="36" src="~/assets/img/show.svg" title=" مشاهده ی ویدیو " alt=" مشاهده ی ویدیو ">
            <span v-if="!show">مشاهده ی ویدیو</span>
            <span v-else>مشاهده ی توضیح</span>
          </button>
        </div>
      </div>
    </div>

</template>
<script>
    export default {
        name: "IntroductionEvent",
      data(){
          return{
            show:false
          }
      },
    }
</script>

<style scoped>
  p{text-align: justify}  @media (max-width: 1075px){.col-md-6 .h-100{padding: 0 !important;}.col-md-6:first-child .h-100 img{width: 100%;height: 100%;}}  @media (max-width: 767px) {.row.align-items-md-stretch{flex-direction: column-revers}.col-md-6:first-child .h-100{display: flex;margin: auto;margin-bottom: 70px;}.col-md-6:first-child .h-100 img {width: 403px;height: auto;text-align: center;justify-content: center;margin: auto}}  @media (max-width: 665px) {.row.align-items-md-stretch{margin-top: -100px}.Introduction-box{margin-bottom: 50px}}  @media (max-width: 518px) {.row.align-items-md-stretch{margin-top: -230px;}.col-md-6:first-child .h-100 img {width: 100%;height: 100%;}}  @media (max-width: 370px) {.row.align-items-md-stretch{margin-top: -300px;}}  .Introduction-box{ display: flex;flex-direction: column;justify-content: center; direction: rtl;}  .show-btn:hover{color: white}  .show-btn{width: 195px;text-align: right;justify-content: right;direction: rtl;background: #6669F1;padding:8px 10px;border-radius: 26px;}
</style>
