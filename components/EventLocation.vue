<template>
  <div class="row align-items-md-stretch header-box">
    <div class="col-md-12 location">
      <a href="https://maps.google.com" title="مکان مسابقه" rel="noreferrer nofollow">
        <img loding="lazy" src="~/assets/img/map.webp" title="مکان مسابقه" alt="مکان مسابقه" width="1210" height="458">
      </a>
    </div>
  </div>
</template>
<script>
    export default {
        name: "EventLocation"
    }
</script>

<style scoped>
 .location img{width: 100%;margin-top: 75px;border-radius: 50px;border: 5px solid white;box-shadow: -2px -2px 45px #c8e3ff;object-fit: cover;height: auto;}  @media (max-width: 991px) {.location img {margin-top: 50px;}}  @media (max-width: 767px) {.location img {border-radius: 20px}}
</style>
