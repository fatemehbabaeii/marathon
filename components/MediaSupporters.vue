<template>
  <div class="row align-items-md-stretch header-box">
    <div class="col-md-12">
      <h2 data-v-7cdef8e2="" class="text-center mt-5 mb-5">حامیان رسانه ای</h2>
    </div>
    <div v-for="media in MediaSupporters" :key="media.id" class="col-lg-2 col-sm-4 col-6 text-center" >
      <div>
        <div class="Event-supporter-box">
          <img loding="lazy" :alt="media.title" :title="media.title" :src="require(`~/assets/img/supporters/${media.imgURL}`)" width="70" height="70" >
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    name: "MediaSupporters",
    data() {
      return {
        MediaSupporters:[
          {title:'ایرانسل' , imgURL: 'iransel.svg',},
          {title:'تپسی' , imgURL: 'tap30.svg',},
          {title:'اسنپ' , imgURL: 'snapp.svg',},
          {title:'کمیته جوانان' , imgURL: 'sp2.svg',},
          {title:'آموت' , imgURL: 'amoot.svg',},
          {title:'بلد' , imgURL: 'balad.svg',},
        ]
      };
    }
  }
</script>

<style scoped>
  .Event-supporter-box{margin-bottom: 10px} .align-items-md-stretch.header-box{margin-top: 100px;position: relative;z-index: 1}.Event-supporter-box div{background: white;margin-top: 25%;border-radius: 40px;padding-top: 5px;width: 47px;height: 47px;}  .Event-supporter-box img{width: 100%;height: 100%;filter: grayscale(1);transform: scale(0.9)}  .Event-supporter-box{background: white;padding: 25px;border-radius: 25px;height: 135px;}  .Event-supporter-box{background: white;padding: 25px;border-radius: 25px;height: 135px;cursor: pointer}  .Event-supporter-box:hover img{filter:unset}  @media (max-width: 991px){.align-items-md-stretch.header-box{margin-top: 30px;}}
</style>
