<template>
  <div class="row align-items-md-stretch header-box">
    <div class="col-md-6">
      <div class="HeaderImg">
       <div class="text-box">
         <p>مسابقه مارتُن <span style="color:#6669F1">برنامـه نویسـی</span></p>
         <p>در سراسر کشور برگزار میکند !</p>
       </div>
        <p class="text-right">لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت تولید ساده</p>
        <div class="text-right btn-box">
          <NuxtLink to="/login" >
          <button class="btn btn-primary btn-more">ورود</button>
          </NuxtLink>
          <NuxtLink to="/Register" >
          <button class="btn btn-primary btn-register">ثبت نام</button>
          </NuxtLink>
        </div>
      </div>
    </div>
    <div class="col-md-6">
      <div class="">
        <img loding="lazy" src="~/assets/img/MarathonHeader.svg" class="MarathonHeader" alt="ماراتن" title="ماراتن" width="978" height="725">
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "TopHeader"
    }
</script>

<style scoped>
.row.align-items-md-stretch.header-box{position: relative;z-index: 1}  .text-box p{color: #334155; font-family: 'IRANYekanExtraBlack';  font-style: normal;  font-weight: 900;  font-size: 41px;  line-height: 71px; letter-spacing: -0.025em; }  .HeaderImg p.text-right{text-align: justify}.HeaderImg{margin-top: 60px;text-align: right;padding-right: 250px;}.MarathonHeader{transform: rotateY(180deg);margin-left: -45px;}  .header-box{margin-top: 60px}.btn-register{background: #6669F1;border-radius: 30px;width:132px;padding: 10px }  .btn-more{background: transparent;color: #99A4B4;border-color: #99A4B4;border-radius: 30px;padding: 10px;width: 132px;}  @media (max-width: 1710px){.HeaderImg {padding-right: 195px;}}  @media (max-width: 1500px){.HeaderImg {padding-right: 120px;}.MarathonHeader{position: relative;left: 170px;}}  @media (max-width: 1400px){.HeaderImg {padding-right: 100px;}}  @media (max-width: 1300px){.HeaderImg {padding-right: 15px;padding-left: 15px}.MarathonHeader {position: relative;left: 317px;}}
 @media (max-width: 1200px){.text-box p {font-weight: 500;font-size: 35px;line-height: 55px;}.MarathonHeader {width: 760px;position: relative;left: 117px;}}  @media (max-width: 1100px){.MarathonHeader {width: 658px;position: relative;left: 117px;}.HeaderImg img{width: 125%;height: 100%}} @media (max-width: 991px){.text-box p{font-weight: 500;font-size: 30px;line-height: 35px;}.HeaderImg{margin-top: 35px;}.MarathonHeader{margin-top: -72px;}.header-box{margin-top: 0}}  @media (max-width: 860px){.text-box p{font-weight: 500;font-size: 25px;line-height: 30px;}.btn-more,.btn-register{font-size: 14px}}  @media (max-width: 767px){.HeaderImg p.text-right,.btn-box{text-align: center !important;}.text-box p {font-weight: 500;font-size: 40px;line-height: 49px;text-align: center;}.MarathonHeader{width: 100%;left: 0;top:50px;}.text-box{margin-top: 60px}.HeaderImg{margin-top: 10px;}}  @media (max-width: 670px){.MarathonHeader{top: 0;}}  @media (max-width: 550px){.MarathonHeader{top: -30px;}.text-box p {font-size: 32px;line-height: 38px;text-align: center;}.HeaderImg p.text-right{font-size: 13px}}
 @media (max-width: 442px){.MarathonHeader{top: -72px;}.text-box p{font-size: 25px;line-height: 30px;text-align: center;}.HeaderImg p.text-right{font-size: 12px}} @media (max-width: 370px){.text-box{margin-top: 45px;}.text-box p {font-size: 22px;line-height: 26px;}.MarathonHeader{top: -105px;}}
</style>
