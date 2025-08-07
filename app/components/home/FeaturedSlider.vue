<template>
  <section class="py-12 bg-white">
    <div class="max-w-7xl mx-auto px-4 space-y-12">
      <!-- TIÊU ĐỀ -->
      <div class="text-center">
        <h2
          class="text-2xl md:text-3xl font-bold text-black relative inline-block"
        >
          <span class="px-4">VINH HẠNH ĐỒNG HÀNH CÙNG THƯƠNG HIỆU</span>
          <div
            class="absolute left-0 right-0 top-1/2 transform -translate-y-1/2 border-t border-gray-400 z-[-1]"
          ></div>
        </h2>
      </div>

      <!-- DANH MỤC -->
      <div
        class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-6 gap-6 text-center"
      >
        <div v-for="(trend, index) in trends" :key="index" class="space-y-2">
          <img
            :src="trend.image"
            :alt="trend.label"
            class="w-full h-32 object-cover rounded-xl shadow"
          />
          <p class="text-sm font-medium text-black uppercase">
            {{ trend.label }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const trends = [
  {
    label: "VÒNG - LẮC",
    image: "images/brand_1.png",
  },
  {
    label: "NHẪN",
    image: "images/brand_2.png",
  },
  {
    label: "DÂY CHUYỀN",
    image: "images/brand_3.png",
  },
  {
    label: "BÔNG TAI",
    image: "images/brand_4.png",
  },
  {
    label: "CHARM PANDORA",
    image: "images/brand_5.png",
  },
  {
    label: "KHUYÊN XỎ",
    image: "images/brand_6.png",
  },
];
</script>

<style scoped>
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css");
</style>
