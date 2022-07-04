<template>
  <div>
    <TopHeader />
    <div class="container py-4">
    <IntroductionEvent />
      <EventDate />
      <EventLocation />
      <CompetitionAreas />
      <EventsAwards />
      <EventsReferees />
      <EventSupporters />
      <MediaSupporters />
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style>
  .container{max-width: 1250px;}
</style>
