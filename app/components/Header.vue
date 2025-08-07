<template>
  <header class="w-full bg-[#3138C0] shadow-sm text-white">
    <div
      class="max-w-screen-xl mx-auto flex items-center justify-between py-2 px-4"
    >
      <!-- Logo -->
      <div class="flex items-center gap-2">
        <span class="text-white text-sm font-semibold">
          Chăm Sóc Xe Phú Giáo
        </span>
      </div>

      <!-- Desktop Navigation -->
      <nav class="hidden md:flex items-center gap-4 text-sm font-semibold">
        <span class="text-white">TRANG CHỦ</span>
        <span class="text-white/30">◊</span>
        <span class="text-white hover:text-orange-400 cursor-pointer">
          GIỚI THIỆU
        </span>
        <span class="text-white/30">◊</span>
        <span class="text-white hover:text-orange-400 cursor-pointer">
          DỊCH VỤ
        </span>
        <span class="text-white/30">◊</span>
        <span class="text-white hover:text-orange-400 cursor-pointer">
          HỆ THỐNG
        </span>
        <span class="text-white/30">◊</span>
        <span class="text-white hover:text-orange-400 cursor-pointer">
          TUYỂN DỤNG
        </span>
        <span class="text-white/30">◊</span>
        <span class="text-white hover:text-orange-400 cursor-pointer">
          TIN TỨC
        </span>
        <span class="text-white/30">◊</span>
        <span class="text-white hover:text-orange-400 cursor-pointer">
          LIÊN HỆ
        </span>
      </nav>

      <!-- Mobile Hamburger -->
      <button
        class="md:hidden text-white focus:outline-none"
        @click="toggleMenu"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>
      </button>
    </div>

    <!-- Mobile Menu -->
    <div
      v-if="menuOpen"
      class="md:hidden px-4 py-2 space-y-2 bg-[#3138C0] text-white shadow-md"
    >
      <span class="block text-white">TRANG CHỦ</span>
      <span class="block text-white hover:text-orange-400">GIỚI THIỆU</span>
      <span class="block text-white hover:text-orange-400">DỊCH VỤ</span>
      <span class="block text-white hover:text-orange-400">HỆ THỐNG</span>
      <span class="block text-white hover:text-orange-400">TUYỂN DỤNG</span>
      <span class="block text-white hover:text-orange-400">TIN TỨC</span>
      <span class="block text-white hover:text-orange-400">LIÊN HỆ</span>
    </div>
  </header>
</template>

<script setup>
import { ref } from "vue";
const menuOpen = ref(false);
function toggleMenu() {
  menuOpen.value = !menuOpen.value;
}
</script>
