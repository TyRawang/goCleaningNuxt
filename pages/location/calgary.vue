<template>
  <section class="go-cleaning-page">
    <ThePageBannerSection :pageMaterials="bannerPageMaterials" />

    <TheQuoteRequestInfoSection />
  </section>
</template>

<script>
import ThePageBannerSection from "@/components/shared/ThePageBannerSection";
import TheQuoteRequestInfoSection from "@/components/shared/TheQuoteRequestInfoSection";
export default {
name: "calgary",
  components: {TheQuoteRequestInfoSection, ThePageBannerSection},

  data(){
    return {
      bannerPageMaterials: {
        bannerImage: '/img/go-cleaning-calgary-banner-bg.png',
        pageTitle: 'Calgary',
        pageSubtitle: 'Perfection is our passion',
        hasButton: false
      }
    }
  }, 
  head() {
    return {
      title: 'Best Commercial & Residential Cleaning in Calgary | Go Cleaning Calgary', 
      meta: [{
        hid: 'description',
        name: 'description', 
        content: 'Go Cleaning is a fast growing company, and Go Cleaning is very proud it. Request a FREE QUOTE for Commercial & Residential Cleaning today'
        // content: 'Let us be your perfect solution for you residential & commercial cleaning needs. Our pricing is Affordable, order your FREE QUOTE today!'
      }]
    }
  }
}
</script>

<style scoped>

</style>
