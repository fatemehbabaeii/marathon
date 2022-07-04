<template>
  <div class="row align-items-md-stretch event-Date bg-white ">
    <div class="col-lg-3 col-sm-4">
      <div class="Event-Box">
        <div class="Event-Timer">
          <img src="~/assets/img/Calendar.svg" loding="lazy" width="24" height="24" alt="تاریخ رویداد" title="تاریخ رویداد">
        </div>
        <div class="Event-Timer-Box">
          <p>تاریخ رویداد</p>
          <span> 5 تیر 1401</span>
        </div>
      </div>
    </div>
    <div class="col-lg-3 col-sm-4">
      <div class="Event-Box">
        <div class="Event-Timer">
          <img loding="lazy" src="~/assets/img/Time Square.svg" width="24" height="24" alt="تاریخ رویداد" title="تاریخ رویداد">
        </div>
        <div class="Event-Timer-Box">
          <p>تاریخ رویداد</p>
          <span> 5 تیر 1401</span>
        </div>
      </div>
    </div>
    <div class="col-lg-3 col-sm-4">
      <div class="Event-Box">
        <div class="Event-Timer">
          <img loding="lazy" src="~/assets/img/Location.svg" width="24" height="24" alt="تاریخ رویداد" title="تاریخ رویداد">
        </div>
        <div class="Event-Timer-Box">
          <p>تاریخ رویداد</p>
          <span> 5 تیر 1401</span>
        </div>
      </div>
    </div>
    <div class="col-lg-3 col-md-12">
      <div class="Event-Box">
        <client-only placeholder="loading...">
        <Countdown deadline="July 23, 2022"></Countdown>
        </client-only>
      </div>
    </div>
  </div>
</template>

<script>
  import Countdown from 'vuejs-countdown'
    export default {
      name: "EventDate",
      components: { Countdown },
    }
</script>

<style scoped>
.vuejs-countdown li:last-child .digit{width: 45px}  .event-Date{border-radius: 20px;padding: 20px;text-align: center;margin-top: 100px;}  .Event-Box{border-left: 1px solid #EBEBEB;display: flex;padding: 10px}  .col-lg-3:nth-child(3) .Event-Box{border-left: 0}
@media (max-width: 1286px){.event-Date{margin-right: 15px;margin-left: 15px}.event-Date .col-lg-3{padding: 0}}  @media (max-width: 991px){.col-sm-4{margin-bottom: 10px}}  @media (max-width: 575px){.Event-Box{border-left: 0}}
p{font-family: IRANYekanExtraBold;font-style: normal;font-weight: 800;font-size: 15px;line-height: 26px;}  .col-lg-3:last-child .Event-Box{height:100%;border-left: 0 solid #EBEBEB;justify-content: center;background: #6669f1;border-radius: 15px;color: white;padding: 10px}  .Event-Timer{flex: 1;margin-top: 20px;}.Event-Timer-Box{flex: 4;}  .vuejs-countdown{direction: ltr}
</style>
