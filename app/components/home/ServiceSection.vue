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
    name: "Bông tai bạc Ý S925 nữ mạ bạch kim đính đá CZ hình trái tim",
    code: "LILI_991582",
    price: "823.000₫",
    image: "images/dv_1.png",
    colors: ["#f50057", "#9c27b0", "#2196f3", "#00bcd4"],
  },
  {
    name: "Nhẫn bạc nữ đính đá CZ hoa bướm",
    code: "LILI_661591",
    price: "753.000₫",
    image: "images/dv_2.png",
  },
  {
    name: "Nhẫn đôi bạc free size đính đá CZ hiệp sĩ và công chúa",
    code: "LILI_819229",
    price: "1.560.000₫",
    image: "images/dv_3.png",
  },
  {
    name: "Dây chuyền bạc nữ đính kim cương Moissanite tròn cách điệu",
    code: "LILI_413898",
    price: "1.619.000₫ – 1.620.000₫",
    image: "images/dv_4.png",
    colors: ["#d9a47e", "#d9bca3"],
  },
  {
    name: "Dây chuyền bạc nữ đính kim cương tự nhiên cỏ 4 lá Lucky",
    code: "LILI_832459",
    price: "1.297.000₫ – 1.329.000₫",
    image: "images/dv_5.png",
    colors: ["#d2b49c", "#eee2d4"],
  },
  {
    name: "Lắc tay bạc Ta S999 nữ cỏ 4 lá cách điệu đẹp",
    code: "LILI_661577",
    price: "1.165.000₫ – 1.187.000₫",
    image: "images/dv_6.png",
    colors: ["#ccc", "#2196f3"],
  },
  {
    name: "Lắc tay bạc nữ đính đá CZ hình trái tim Heart Of The Sea",
    code: "LILI_427425",
    price: "1.534.000₫",
    image: "images/dv_7.png",
  },
  {
    name: "Lắc tay bạc cặp đôi tình yêu tình bạn vĩnh cửu Forever",
    code: "LILI_818622",
    price: "1.664.000₫",
    image: "images/dv_8.png",
  },
];
</script>
