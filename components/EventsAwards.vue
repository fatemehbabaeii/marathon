<template>
  <div class="row align-items-md-stretch header-box">
    <div class="col-md-6 Competition-Area text-right">
      <h2 class="text-right mt-5 mb-5">جوایــز اهدایی ویژه برای نفرات اول تا سوم</h2>
      <div v-for="Award in Awards" :key="Award.id" class="col-md-12 p-0" >
        <div class="Competition-Area-box">
          <span class="number">{{ Award.number }}</span>
          <span class="Competition-number"> {{ Award.position}} </span>
          <span class="Competition_awards"><span>{{ Award.award }}</span> بهار آزادی</span>
        </div>
      </div>
      <div class="col-md-12 p-0">
        <div class="Awards-input">
          <label class="w-100">
            <input v-model.trim="name" placeholder="نام خود را وارد کنید" @keyup="setCookie">
          </label>
        </div>
      </div>
    </div>
    <div class="col-md-6 Competition-Area Awards">
      <img loding="lazy" src="~/assets/img/Awards.svg" width="566" height="450"
           title="جوایــز اهدایی ویژه برای نفرات اول تا سوم" alt="جوایــز اهدایی ویژه برای نفرات اول تا سوم">
      <span>{{ WinnerName }}</span>
    </div>
  </div>
</template>

<script>
  export default {
    name: "EventsAwards",
    data() {
      return {
        name: '',
        WinnerName: this.$cookies.get('EventsAwards'),
        Awards: [
          {number: 1, position: "نفر اول :", award: '5 عدد سکه',},
          {number: 2, position: "نفر دوم :", award: '3 عدد سکه',},
          {number: 3, position: "نفر سوم :", award: '1 عدد سکه',},]
      }
    },
    methods: {
      setCookie() {
        this.WinnerName = this.name
        this.$cookies.set("EventsAwards", this.name, {
          path: '/',
          maxAge: 60 * 60 * 24 * 7
        });
      }
    }
  }
</script>

<style scoped>
  .Awards img{width: 100%}.Awards{margin-top: 35px;}.align-items-md-stretch.header-box{ margin-top: 70px;}.Competition-Area.Awards span{top: 0;position: absolute;left: calc(100% - 50%);transform: translate(-50%, -33px);font-style: normal;font-weight: 800;font-size: 16px;line-height: 28px;justify-content: center;border-radius: 15px;}  .number{background: #6669F1;box-shadow: 0px 20px 35px rgb(102 105 241 / 35%);width: 44px;height: 44px;border-radius: 25px;display: inline-block;text-align: center;font-style: normal;font-weight: 700;font-size: 25px;color: white;line-height: 189.23%;letter-spacing: 0.01em;}  .Competition-number{font-family: 'IRANYekanRegular';font-style: normal;font-weight: 700;font-size: 25px;text-align: right;letter-spacing: 0.01em;color: #A1AFC4;padding-right: 10px;}  .Competition_awards{font-family: 'IRANYekanExtraBlack';font-style: normal;font-weight: 900;font-size: 28px;line-height: 52px;text-align: center;letter-spacing: -0.035em;}  .Competition_awards span{color: #6669f1;margin-right: 11px;}  .Competition-Area-box{padding: 15px;border-radius: 15px;border-radius: 30px;display: inline-block;cursor: pointer}  .Competition-Area-box:hover{background: #FFFFFF;box-shadow: 0px 4px 45px rgb(76 142 208 / 25%)}  .Awards-input{width: 442px}  .Awards-input input{width: 100%;border-radius: 30px;border: 1px solid #6669f1;background: transparent;padding: 15px;margin-top: 15px;color: #929FB2;margin-top: 25px;}  :focus-visible {outline: -webkit-focus-ring-color auto 0;}  @media (max-width: 1007px){.Awards-input input{width: 89%;}h2{font-size: 20px}.Competition_awards span{color: #6669f1;margin-right: 0;}.Competition-number{font-size: 20px;}.Competition_awards{font-size: 25px;}.Competition_awards span {margin-right: 0;}}  @media (max-width: 879px){.Awards-input input{width: 75%;}.number{width: 35px;height: 35px;font-size: 20px;font-family: 'IRANYekanFaNum'}h2{font-size: 18px}.Competition_awards span{color: #6669f1;margin-right: 0;}.Competition-number{font-size: 18px;}.Competition_awards{font-size: 21px;}.Competition_awards span {margin-right: 0;}}  @media (max-width: 767px){.Awards-input label input{font-size: 14px}.Awards-input{width: unset}.Awards-input label{width: 543px !important;margin-bottom: 30px;}.Competition-Area{text-align: center !important;}h2{font-size: 21px;text-align: center !important;}.number{width: 45px;height: 45px;font-size: 26px;}.Competition-number{font-size: 23px}.Competition_awards{font-size: 25px;}}  @media (max-width: 547px){.Awards-input label{width: 100% !important;}}  @media (max-width: 458px){.Competition-Area.Awards span{transform: translate(-50%, 0px);}.Competition-Area{font-size: 20px}h2{font-size: 18px;}.number{width: 36px;height: 36px;font-size: 21px;}.Competition-number{font-size: 20px}.Competition_awards{font-size: 20px;}.Competition-Area-box{padding: 10px;}}  @media (max-width: 404px){.Competition-Area.Awards span{transform: translate(-50%, 40%);}}  @media (max-width: 384px){.Awards{margin-top: 0;}.Competition-Area.Awards span{transform: translate(-50%,35px);}h2{font-size: 15px;margin-bottom: 20px !important;}.Competition-Area{font-size: 20px}h2{font-size: 18px;}.number{width: 30px;height: 30px;font-size: 18px;}.Competition-number{font-size: 17px;padding-right: 0}.Competition_awards{font-size: 18px;}.Competition-Area-box{padding: 5px;}}  @media (max-width: 340px){.Competition-Area.Awards span{transform: translate(-50%,50px);}}
</style>
