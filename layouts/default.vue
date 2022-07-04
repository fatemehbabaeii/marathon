<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-light">
      <div class="container-fluid">
        <button  class="navbar-toggler" type="button" v-on:click="show = !show" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div id="navbarNavAltMarkup" class="collapse navbar-collapse"  :class="show?'show':''">
          <div class="navbar-nav">
            <a class="nav-link active" aria-current="page" href="#">معرفی و توضیح مسابقه</a>
            <a class="nav-link" href="#">حوزه ی مسابقه</a>
            <a class="navbar-brand" href="#">لوگو</a>
            <a class="nav-link" href="#">جوایز</a>
            <a class="nav-link ">داورران و سرمایه گذاران</a>
          </div>
        </div>
      </div>
    </nav>
    <Nuxt />
    <div class="footer">
      <ul class="list-group list-group-horizontal">
        <li v-for="SocialMedia in SocialMedias" :key="SocialMedia.id" class="list-group-item" >
          <div>
            <a :href="SocialMedia.link">
            <img loding="lazy" :alt="SocialMedia.title" :title="SocialMedia.title" :src="require(`~/assets/img/${SocialMedia.imgURL}`)" width="20" height="20" >
            </a>
          </div>
        </li>
      </ul>
      <p class="text-center">کلیه حقوق متعلق به لورم ایپسوم می باشد</p>
    </div>
  </div>
</template>
<script>
  export default {
    name: "DefaultLayouts",
    data() {
      return {
        SocialMedias:[
          {title:'اینستاگرام' , imgURL: 'instagram.svg',link:'https://instagram.com'},
          {title:'لینکدین' , imgURL: 'linkedin.svg',link:'https://linkedin.com'},
          {title:'توییتر' , imgURL: 'twitter.svg',link:'https://twitter.com'},
          {title:'فیس بوک' , imgURL: 'facebook.svg',link:'https://facebook.com'},
        ],
        show:false
      }
    },
  }
</script>
<style>
  #navbarNavAltMarkup{justify-content: center;}  .navbar a{color: #4D596B;}  .collapse.show{display: block}  .navbar-collapse.show{background: white;text-align: right;border-radius: 6px;}  .navbar-light .navbar-brand{font-style: normal;font-weight: 700;font-size: 28px;color: #6669F1}  .footer{padding-top: 250px;position: relative}  .footer:before{content: '';display:block;background-image:url(~assets/img/bg-blue.svg); width: 100%;height:750px;position: absolute;top: -514px;background-size:cover;background-position:bottom  }  .list-group-item{background-color: #fff0;border: 0px solid rgba(0, 0, 0, 0.125);}  .list-group-horizontal{justify-content: center;padding: 0}  .list-group-item div{border: 1px solid #a1afc3;border-radius: 10px;margin: 10px;width: 35px;height: 35px;text-align: center;padding-top: 3px;}  .list-group-item {position: relative;display: block;padding: 0}  .list-group-item img{filter: grayscale(1);opacity: .8;cursor: pointer;margin-top: -10px}  .list-group-item div:hover img{filter: grayscale(0);opacity: 1;}.list-group-horizontal > .list-group-item + .list-group-item {border-top-width: 0;}
  @media (max-width: 767px){.list-group img{margin-top: -12px;}}  @media (max-width: 482px){.h-100  img{margin-top: 0;}}
</style>
