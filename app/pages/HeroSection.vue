<template>
    <section class="relative">
        <Swiper
            :modules="[Autoplay, Pagination]"
            :autoplay="{ delay: 4000, disableOnInteraction: false }"
            :pagination="{ clickable: true }"
            loop
            class="h-[300px] sm:h-[400px] md:h-[500px] w-full"
        >
            <SwiperSlide v-for="(img, index) in images" :key="index">
                <div class="w-full h-full">
                    <img
                        :src="img"
                        alt="Slide Image"
                        class="w-full h-full object-cover"
                    />
                </div>
            </SwiperSlide>
        </Swiper>

        <!-- Optional: overlay text -->
        <div class="absolute inset-0 flex items-center justify-center">
            <h1
                class="text-white text-3xl md:text-5xl font-bold drop-shadow-lg"
            >
                Chào mừng đến với Phú Giáo Academy
            </h1>
        </div>
    </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination } from "swiper/modules";

import "swiper/css";
import "swiper/css/pagination";

const images = ["images/hero_1.png", "images/hero_2.png"];
</script>

<style scoped>
:deep(.swiper-pagination-bullet-active) {
    background: #1e40af;
}
</style>
