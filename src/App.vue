<template>
  <navbar></navbar>
  <landing></landing>
  <informations></informations>
  <location></location>
  <service></service>
  <footerV></footerV>
</template>
<style src='./assets/css/main.css'></style>
<script>
import navbar from "@/components/navbars/nav-bar.vue"
import landing from "@/components/landing/landing-view.vue"
import informations from "@/components/informations/information-about.vue"
import location from "@/components/location/location-main.vue"
import service from "@/components/service/service-view.vue"
import footerV from "@/components/footer/footer-view.vue"
export default {
  name: 'App',
  components: {
    navbar,
    landing,
    informations,
    location,
    service,
    footerV
  }
}
</script>

<style>

</style>
