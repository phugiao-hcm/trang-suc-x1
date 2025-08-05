<template>
    <header
        class="bg-white border-b border-pink-200 shadow-sm sticky top-0 z-50"
    >
        <div
            class="max-w-7xl mx-auto px-4 py-3 flex items-center justify-between"
        >
            <!-- Logo -->
            <NuxtLink to="/" class="flex items-center space-x-2">
                <img src="/images/avt_1.png" alt="Logo" class="h-8 w-auto" />
                <span
                    class="hidden sm:inline font-semibold text-red-600 text-sm"
                >
                    Premium Jewelry
                </span>
            </NuxtLink>

            <!-- Search (desktop only) -->
            <div class="hidden md:flex flex-1 mx-6">
                <input
                    type="text"
                    placeholder="Tìm kiếm sản phẩm..."
                    class="w-full border border-gray-300 rounded-full px-4 py-2 text-sm focus:outline-none focus:border-pink-400"
                />
            </div>

            <!-- Account + Cart -->
            <div class="flex items-center space-x-4 text-sm">
                <!-- Toggle button (mobile only) -->
                <button
                    class="md:hidden text-pink-600"
                    @click="menuOpen = !menuOpen"
                >
                    <i class="fas fa-bars text-lg"></i>
                </button>

                <!-- Tài khoản -->
                <NuxtLink
                    to="/"
                    class="hidden md:flex items-center space-x-1 hover:text-pink-500"
                >
                    <i class="fas fa-user"></i>
                    <span>Tài khoản</span>
                </NuxtLink>

                <!-- Giỏ hàng -->
                <NuxtLink
                    to="/"
                    class="relative hidden md:flex items-center space-x-1 hover:text-pink-500"
                >
                    <i class="fas fa-box"></i>
                    <span>Giỏ hàng</span>
                    <span
                        class="absolute -top-2 -right-2 bg-red-500 text-white rounded-full text-xs w-5 h-5 flex items-center justify-center"
                        >0</span
                    >
                </NuxtLink>
            </div>
        </div>

        <!-- Desktop nav -->
        <nav class="border-t border-pink-200 hidden md:block">
            <div class="max-w-7xl mx-auto px-4">
                <ul
                    class="flex flex-nowrap justify-center items-center text-sm font-medium text-gray-700 py-2 space-x-4 overflow-x-auto whitespace-nowrap"
                >
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-600"
                            >VÒNG - LẮC</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-600"
                            >NHẪN</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-600"
                            >DÂY CHUYỀN</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-600"
                            >BÔNG TAI</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-600"
                            >KHUYẾN XẺ</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-600"
                            >TRANG SỨC ĐÔI</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-600"
                            >PHONG THỦY</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-600"
                            >QUÀ TẶNG</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-600"
                            >PHỤ KIỆN</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-600"
                            >SẢN PHẨM MỚI</NuxtLink
                        >
                    </li>
                </ul>
            </div>
        </nav>

        <!-- Mobile menu -->
        <div
            v-if="menuOpen"
            class="md:hidden border-t border-pink-200 bg-white px-4 py-2 space-y-2 text-sm font-medium"
        >
            <NuxtLink to="/" class="block hover:text-pink-600"
                >VÒNG - LẮC</NuxtLink
            >
            <NuxtLink to="/" class="block hover:text-pink-600">NHẪN</NuxtLink>
            <NuxtLink to="/" class="block hover:text-pink-600"
                >DÂY CHUYỀN</NuxtLink
            >
            <NuxtLink to="/" class="block hover:text-pink-600"
                >BÔNG TAI</NuxtLink
            >
            <NuxtLink to="/" class="block hover:text-pink-600"
                >KHUYẾN XẺ</NuxtLink
            >
            <NuxtLink to="/" class="block hover:text-pink-600"
                >TRANG SỨC ĐÔI</NuxtLink
            >
            <NuxtLink to="/" class="block hover:text-pink-600"
                >PHONG THỦY</NuxtLink
            >
            <NuxtLink to="/" class="block hover:text-pink-600"
                >QUÀ TẶNG</NuxtLink
            >
            <NuxtLink to="/" class="block hover:text-pink-600"
                >PHỤ KIỆN</NuxtLink
            >
            <NuxtLink to="/" class="block hover:text-pink-600"
                >SẢN PHẨM MỚI</NuxtLink
            >
        </div>
    </header>
</template>

<script setup>
import { ref } from "vue";
const menuOpen = ref(false);
</script>

<style scoped>
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css");

nav ul::-webkit-scrollbar {
    display: none;
}
</style>
