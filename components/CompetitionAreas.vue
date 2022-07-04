<template>
  <div>
    <h2 class="text-center mt-5 mb-5">حوزه های مسابقه</h2>
    <div class="row align-items-md-stretch header-box gap-2">
      <div  v-for="competition in CompetitionAreas" :key="competition.id" class="col-md-6 col-lg-3 mt-4">
        <div class="Competition-Area">
        <div class="d-flex text-right mt-3">
          <div class="d-flex-2">
            <div class="Competition-Area-img">
              <img loding="lazy" width="23" height="22" :alt="competition.title" :title="competition.title" :src="require(`~/assets/img/${competition.imgURL}`)" >
            </div>
          </div>
          <p class="d-flex-7">{{ competition.title }}</p>
        </div>
        <div>
          <p class="text-right Competition-p">
             {{ competition.text }}
          </p>
        </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
    export default {
        name: "CompetitionAreas",
      data() {
        return {
          CompetitionAreas:[
            {imgURL: 'Icon1.svg',title:"لورم اپیسیوم" ,text:' لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده از طراحان گرافیک است،' , },
            {imgURL: 'Icon2.svg',title:"لورم اپیسیوم" ,text:' لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده از طراحان گرافیک است،' , },
            {imgURL: 'Icon3.svg',title:"لورم اپیسیوم" ,text:' لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده از طراحان گرافیک است،' , },
            {imgURL: 'icon4.svg',title:"لورم اپیسیوم" ,text:' لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده از طراحان گرافیک است،' , },
            {imgURL: 'Icon1.svg',title:"لورم اپیسیوم" ,text:' لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده از طراحان گرافیک است،' , },
            {imgURL: 'Icon2.svg',title:"لورم اپیسیوم" ,text:' لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده از طراحان گرافیک است،' , },
            {imgURL: 'Icon3.svg',title:"لورم اپیسیوم" ,text:' لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده از طراحان گرافیک است،' , },
            {imgURL: 'icon4.svg',title:"لورم اپیسیوم" ,text:' لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده از طراحان گرافیک است،' , },
          ]
        };
      }
    }
</script>

<style scoped>
  .Competition-Area{padding:15px;cursor:pointer;border: 2px solid rgba(188, 220, 248, 0.5);border-radius: 30px;}.d-flex-2{flex: 2;text-align: center;}.d-flex-7{flex: 7;font-style: normal;font-weight: 800;font-size: 16px;line-height: 28px;margin-top: 15px;justify-content: center;display: flex;}  .Competition-Area-img{background: #ffffff;position: relative;border-radius: 15px;z-index: 0;padding: 18px;font-family: IRANYekanExtraBold;font-style: normal;font-weight: 800;font-size: 16px;line-height: 26px;justify-content: center;display: flex;}  .Competition-p{margin-top: 15px;color: #929FB2;text-align: justify !important;} .Competition-Area:hover .Competition-Area-img{background: #6669F1;}.Competition-Area:hover img{filter: brightness(2.5);}  .Competition-Area:hover{background: #FFFFFF}
</style>
