<template>
  <section class="py-12 bg-white">
    <div class="max-w-7xl mx-auto px-4">
      <!-- Flash Sale Header -->
      <div class="flex items-center justify-between mb-6">
        <div class="flex items-center gap-2">
          <img src="/images/flash_sale.png" alt="flash" class="w-6 h-6" />
          <h2 class="text-2xl font-bold text-red-600">FLASH SALE</h2>
          <div class="flex gap-1 text-white text-sm font-semibold ml-4">
            <div
              v-for="(t, i) in timeParts"
              :key="i"
              class="bg-red-600 px-2 py-1 rounded"
            >
              {{ t.value }}<br />
              <span class="text-xs">{{ t.label }}</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Swiper Products -->
      <Swiper
        :modules="[Navigation]"
        :slides-per-view="1.5"
        :space-between="20"
        :breakpoints="{
          640: { slidesPerView: 1.5 },
          768: { slidesPerView: 3 },
          1024: { slidesPerView: 4.5 },
        }"
        navigation
        class="overflow-hidden"
      >
        <SwiperSlide v-for="prod in products" :key="prod.id">
          <div
            class="shadow rounded-lg overflow-hidden bg-white hover:shadow-lg transition"
          >
            <div class="relative">
              <img :src="prod.image" class="w-full h-52 object-cover" />
              <div
                v-if="prod.discount"
                class="absolute top-2 left-2 bg-red-600 text-white text-xs font-bold px-2 py-1 rounded"
              >
                -{{ prod.discount }}%
              </div>
            </div>
            <div class="p-3 text-center">
              <p class="text-sm text-gray-400">
                {{ prod.origin }}
              </p>
              <h3 class="font-semibold text-sm line-clamp-2">
                {{ prod.name }}
              </h3>
              <p class="text-red-600 font-bold">
                {{ prod.price }}
                <span class="text-gray-400 line-through ml-1 text-sm">{{
                  prod.oldPrice
                }}</span>
              </p>
              <button
                class="border mt-3 px-4 py-2 text-sm font-medium rounded w-full hover:bg-purple-100"
              >
                🛍️ CHỌN MUA
              </button>
            </div>
          </div>
        </SwiperSlide>
      </Swiper>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import { Navigation } from "swiper/modules";
import { ref, onMounted } from "vue";

const products = [
  {
    id: 1,
    name: "Rửa xe ô tô tiêu chuẩn",
    price: "80.000₫",
    oldPrice: "100.000₫",
    discount: 20,
    image: "images/km_1.png",
    origin: "Việt Nam",
  },
  {
    id: 2,
    name: "Vệ sinh nội thất ô tô chuyên sâu",
    price: "900.000₫",
    oldPrice: "1.200.000₫",
    discount: 25,
    image: "images/km_2.png",
    origin: "Việt Nam",
  },
  {
    id: 3,
    name: "Đánh bóng sơn xe chuyên nghiệp",
    price: "1.800.000₫",
    oldPrice: "2.200.000₫",
    discount: 18,
    image: "images/km_3.png",
    origin: "Thái Lan",
  },
  {
    id: 4,
    name: "Phủ ceramic bảo vệ sơn 9H",
    price: "4.500.000₫",
    oldPrice: "5.500.000₫",
    discount: 18,
    image: "images/km_4.png",
    origin: "Hàn Quốc",
  },
  {
    id: 5,
    name: "Dán phim cách nhiệt 3M chính hãng",
    price: "7.800.000₫",
    oldPrice: "9.000.000₫",
    discount: 13,
    image: "images/km_5.png",
    origin: "Mỹ",
  },
  {
    id: 6,
    name: "Vệ sinh khoang máy bằng hơi nước nóng",
    price: "300.000₫",
    oldPrice: "400.000₫",
    discount: 25,
    image: "images/km_6.png",
    origin: "Nhật Bản",
  },
  {
    id: 7,
    name: "Phủ gầm chống rỉ sét",
    price: "2.500.000₫",
    oldPrice: "3.000.000₫",
    discount: 17,
    image: "images/km_7.png",
    origin: "Thái Lan",
  },
];

const countdown = ref(36000); // seconds
const timeParts = ref([]);

const updateCountdown = () => {
  const hours = Math.floor(countdown.value / 3600);
  const minutes = Math.floor((countdown.value % 3600) / 60);
  const seconds = countdown.value % 60;
  timeParts.value = [
    { label: "Giờ", value: String(hours).padStart(2, "0") },
    { label: "Phút", value: String(minutes).padStart(2, "0") },
    { label: "Giây", value: String(seconds).padStart(2, "0") },
  ];
};

onMounted(() => {
  updateCountdown();
  setInterval(() => {
    if (countdown.value > 0) {
      countdown.value--;
      updateCountdown();
    }
  }, 1000);
});
</script>

<style scoped>
.line-clamp-2 {
  overflow: hidden;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}
</style>
