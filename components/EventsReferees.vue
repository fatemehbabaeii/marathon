<template>
  <div class="row align-items-md-stretch header-box">
    <div class="col-md-12">
      <h2 data-v-7cdef8e2="" class="text-center mt-5 mb-5">داوران رویداد</h2>
    </div>
    <div v-for="referee in referees" :key="referee.id" class="col-lg-2 col-md-4 col-md-4 col-sm-6  text-center" >
      <div @mouseover="referee.hover = true" @mouseleave="referee.hover = false" style="position: relative">
        <div class="Event-referees-box ">
          <img loding="lazy" :src="require(`~/assets/img/${referee.imgURL}`)" width="70" height="70" :alt="referee.name"
               :title="referee.name">
          <p class="mb-0 mt-2">{{ referee.name }}</p>
          <span>{{ referee.role }}</span>
        </div>
        <div v-if="referee.hover" class="Event-referees-box hover">
          <div>
            <a :href="referee.twitter" rel="noreferrer nofollow">
              <img loding="lazy" src="~/assets/img/twitter.svg" width="23" height="18" alt="twitter" title="twitter">
            </a>
          </div>
          <div class="ml-1 mr-1" rel="noreferrer nofollow">
            <a :href="referee.dribbble">
              <img loding="lazy" src="~/assets/img/dribbble.svg" width="21" height="21" alt="dribbble" title="dribbble">
            </a>
          </div>
          <div>
            <a :href="referee.facebook" rel="noreferrer nofollow">
              <img loding="lazy" src="~/assets/img/facebook.svg" width="21" height="21" alt="facebook" title="facebook">
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "EventsReferees",
      data() {
        return {
          referees:[
            {name:'آناهیتا سلطانی' , role:'مدیر عامل شرکت ایرانسل', imgURL: 'davar1.webp',twitter:'https://twitter.com',facebook:'https://www.facebook.com',dribbble:'https://dribbble.com/',hover: false, },
            {name:'نازنین سلطانی' , role:'مدیر عامل شرکت تپسی', imgURL: 'davar2.webp',twitter:'https://twitter.com',facebook:'https://www.facebook.com',dribbble:'https://dribbble.com/',hover: false,},
            {name:'امیر علی سلطانی' , role:'مدیر عامل شرکت جانبو', imgURL: 'davar1.webp',twitter:'https://twitter.com',facebook:'https://www.facebook.com',dribbble:'https://dribbble.com/',hover: false,},
            {name:'نازنین سلطانی' , role:'مدیر عامل شرکت پارسه', imgURL: 'davar2.webp',twitter:'https://twitter.com',facebook:'https://www.facebook.com',dribbble:'https://dribbble.com/',hover: false,},
            {name:'آناهیتا سلطانی' , role:'مدیر عامل شرکت آموت', imgURL: 'davar1.webp',twitter:'https://twitter.com',facebook:'https://www.facebook.com',dribbble:'https://dribbble.com/',hover: false,},
            ]
        };
      }
    }
</script>

<style scoped>
.align-items-md-stretch.header-box{margin-top: 100px;justify-content: center}.Event-referees-box div{background: white;margin-top: 25%;border-radius: 40px;padding-top: 5px;width: 47px;height: 47px;}  .Event-referees-box.hover{width:100%;height:100%;display: flex;justify-content: center;background: rgba(143, 193, 238, 0.5);backdrop-filter: blur(10px);border-radius: 37px;justify-content: center;position: absolute;top: 0}  .Event-referees-box{cursor:pointer;background: white;border-radius: 37px;padding: 25px;}  .Event-referees-box span{color: #929FB2;font-size: 11px}  .Event-referees-box p{font-style: normal;font-weight: 700;font-size: 14px;line-height: 34px;}  .col-lg-2.col-md-4.col-md-4.col-sm-6{margin-bottom: 15px}
@media (min-width: 991px){.col-lg-2 {flex: 0 0 20%;max-width: 20%;}}  img{border-radius: 40px;}  @media (max-width: 991px){.Event-referees-box div{margin-top: 15%}}  @media (max-width: 475px){.align-items-md-stretch.header-box{margin-top: 0}}
</style>
