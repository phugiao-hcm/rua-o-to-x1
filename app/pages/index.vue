<template>
  <div>
    <HeroSection />
    <InfoSection />
    <FeaturedSlider />

    <FlashSaleSlider />
    <ServiceSection />
    <CustomerFeedback />
  </div>
</template>

<script setup>
import HeroSection from "../components/home/HeroSection.vue";
import FeaturedSlider from "../components/home/FeaturedSlider.vue";
import ServiceSection from "../components/home/ServiceSection.vue";
import CustomerFeedback from "../components/home/CustomerFeedback.vue";
import InfoSection from "../components/home/InfoSection.vue";
import FlashSaleSlider from "../components/home/FlashSaleSlider.vue";
</script>
