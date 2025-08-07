<template>
  <header class="w-full bg-white shadow-sm">
    <div
      class="max-w-screen-xl mx-auto flex items-center justify-between py-2 px-4"
    >
      <!-- Logo -->
      <div class="flex items-center gap-2">
        <!-- <img src="/images/avt_1.png" alt="Logo" class="h-10 w-auto" /> -->
        <span class="text-orange-500 text-sm">Chăm Sóc Xe Phú Giáo</span>
      </div>

      <!-- Desktop Navigation -->
      <nav class="hidden md:flex items-center gap-4 text-sm font-semibold">
        <span class="text-blue-800">TRANG CHỦ</span>
        <span class="text-gray-400">◊</span>
        <span class="text-gray-800 hover:text-blue-600 cursor-pointer"
          >GIỚI THIỆU</span
        >
        <span class="text-gray-400">◊</span>
        <span class="text-gray-800 hover:text-blue-600 cursor-pointer"
          >DỊCH VỤ</span
        >
        <span class="text-gray-400">◊</span>
        <span class="text-gray-800 hover:text-blue-600 cursor-pointer"
          >HỆ THỐNG</span
        >
        <span class="text-gray-400">◊</span>
        <span class="text-gray-800 hover:text-blue-600 cursor-pointer"
          >TUYỂN DỤNG</span
        >
        <span class="text-gray-400">◊</span>
        <span class="text-gray-800 hover:text-blue-600 cursor-pointer"
          >TIN TỨC</span
        >
        <span class="text-gray-400">◊</span>
        <span class="text-gray-800 hover:text-blue-600 cursor-pointer"
          >LIÊN HỆ</span
        >
      </nav>

      <!-- Mobile Hamburger -->
      <button
        class="md:hidden text-gray-700 focus:outline-none"
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
      class="md:hidden px-4 py-2 space-y-2 bg-white shadow-md"
    >
      <span class="block text-blue-800">TRANG CHỦ</span>
      <span class="block text-gray-800">GIỚI THIỆU</span>
      <span class="block text-gray-800">DỊCH VỤ</span>
      <span class="block text-gray-800">HỆ THỐNG</span>
      <span class="block text-gray-800">TUYỂN DỤNG</span>
      <span class="block text-gray-800">TIN TỨC</span>
      <span class="block text-gray-800">LIÊN HỆ</span>
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
