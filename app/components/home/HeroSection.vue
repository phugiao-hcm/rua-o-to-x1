<template>
  <section
    class="text-white py-16 px-4"
    style="
      background-image: url('/images/bg_qt.png');
      background-size: cover;
      background-position: center;
    "
  >
    <div class="z-10 max-w-6xl mx-auto text-center">
      <h2 class="text-3xl md:text-4xl font-extrabold uppercase">
        Quy trình tiếp nhận & rửa xe
      </h2>
      <div class="w-16 h-1 bg-orange-500 mx-auto mt-2 mb-4"></div>
      <p class="max-w-xl mx-auto text-sm md:text-base">
        Đến với chúng tôi khách hàng hoàn toàn yên tâm về chất lượng dịch vụ
      </p>

      <!-- Swiper timeline -->
      <swiper
        :slides-per-view="1.2"
        :space-between="24"
        :breakpoints="{
          640: { slidesPerView: 2 },
          768: { slidesPerView: 3 },
          1024: { slidesPerView: 6 },
        }"
        class="mt-12"
      >
        <swiper-slide
          v-for="(step, index) in steps"
          :key="index"
          class="flex flex-col items-center justify-between text-center"
        >
          <!-- Circle Number -->
          <div class="flex flex-col items-center">
            <div
              class="bg-[#3138C0] w-20 h-20 rounded-full flex items-center justify-center text-2xl font-bold mb-2"
            >
              {{ step.number }}
            </div>

            <!-- Vertical line -->
            <div class="w-1 h-4 bg-white opacity-50 mb-2"></div>
          </div>

          <!-- Content -->
          <div class="text-center">
            <p class="font-bold text-sm">{{ step.title }}</p>
            <p class="text-xs leading-tight mt-1">{{ step.desc }}</p>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section>
</template>
  
  <script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";

const steps = [
  {
    number: "01",
    title: "TIẾP NHẬN XE",
    desc: "Dịch vụ chăm sóc ô tô - xe máy chuyên nghiệp",
  },
  {
    number: "02",
    title: "LÊN BÊN XE",
    desc: "Dịch vụ chăm sóc ô tô - xe máy chuyên nghiệp",
  },
  {
    number: "03",
    title: "RỬA XE",
    desc: "Dịch vụ chăm sóc ô tô - xe máy chuyên nghiệp",
  },
  {
    number: "04",
    title: "LÀM SẠCH BỀ NGOÀI XE",
    desc: "Dịch vụ chăm sóc ô tô - xe máy chuyên nghiệp",
  },
  {
    number: "05",
    title: "LAU KHÔ",
    desc: "Dịch vụ chăm sóc ô tô - xe máy chuyên nghiệp",
  },
  {
    number: "06",
    title: "GIAO XE",
    desc: "Dịch vụ chăm sóc ô tô - xe máy chuyên nghiệp",
  },
];
</script>
  
  <style scoped>
/* Tuỳ chọn: có thể thêm shadow hoặc hiệu ứng khác tại đây */
</style>
  