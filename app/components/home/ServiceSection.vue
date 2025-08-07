<template>
  <section class="py-12 bg-white">
    <div class="max-w-7xl mx-auto px-4">
      <!-- Tiêu đề -->
      <div class="text-center mb-10">
        <h2
          class="text-2xl md:text-3xl font-bold text-black relative inline-block"
        >
          <span class="px-4">DỊCH VỤ CAR</span>
          <div
            class="absolute left-0 right-0 top-1/2 transform -translate-y-1/2 border-t border-gray-300 z-[-1]"
          ></div>
        </h2>
      </div>

      <!-- Danh sách sản phẩm -->
      <div
        class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6"
      >
        <div
          v-for="(product, index) in products"
          :key="index"
          class="bg-gray-50 rounded-lg overflow-hidden shadow hover:shadow-md transition"
        >
          <!-- Ảnh -->
          <img
            :src="product.image"
            :alt="product.name"
            class="w-full h-[240px] object-cover"
          />

          <!-- Nội dung -->
          <div class="p-4 space-y-2">
            <p class="text-sm text-gray-800 leading-snug">
              {{ product.name }}<br />
              <span class="text-gray-500 text-xs">{{ product.code }}</span>
            </p>

            <!-- Giá -->
            <p class="text-sm font-bold text-red-600">
              {{ product.price }}
            </p>

            <!-- Màu (nếu có) -->
            <div v-if="product.colors" class="flex space-x-1 mt-2">
              <div
                v-for="(color, i) in product.colors"
                :key="i"
                class="w-4 h-4 rounded border border-gray-300"
                :style="{ backgroundColor: color }"
              ></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const products = [
  {
    name: "Rửa xe ô tô tiêu chuẩn",
    code: "DV_OTO_01",
    price: "80.000₫",
    image: "images/dv_1.png",
    colors: ["#f50057", "#9c27b0", "#2196f3", "#00bcd4"], // Có thể dùng làm phân loại xe
  },
  {
    name: "Rửa gầm & vệ sinh khoang máy",
    code: "DV_OTO_02",
    price: "250.000₫",
    image: "images/dv_2.png",
  },
  {
    name: "Rửa xe ô tô + vệ sinh nội thất",
    code: "DV_OTO_03",
    price: "400.000₫",
    image: "images/dv_3.png",
  },
  {
    name: "Dán phim cách nhiệt 3M chính hãng",
    code: "DV_OTO_04",
    price: "6.500.000₫ – 8.500.000₫",
    image: "images/dv_4.png",
    colors: ["#d9a47e", "#d9bca3"], // Có thể là màu phim
  },
  {
    name: "Dán decal đổi màu toàn bộ xe",
    code: "DV_OTO_05",
    price: "9.000.000₫ – 15.000.000₫",
    image: "images/dv_5.png",
    colors: ["#d2b49c", "#eee2d4"], // Các màu dán
  },
  {
    name: "Dán PPF bảo vệ sơn",
    code: "DV_OTO_06",
    price: "15.000.000₫ – 25.000.000₫",
    image: "images/dv_6.png",
    colors: ["#ccc", "#2196f3"],
  },
  {
    name: "Vệ sinh & đánh bóng nội thất",
    code: "DV_OTO_07",
    price: "1.200.000₫",
    image: "images/dv_7.png",
  },
  {
    name: "Phủ gầm chống rỉ sét",
    code: "DV_OTO_08",
    price: "2.500.000₫",
    image: "images/dv_8.png",
  },
];
</script>
