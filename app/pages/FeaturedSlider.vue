<template>
    <section class="py-12 bg-white">
        <div class="max-w-7xl mx-auto px-4 space-y-12">
            <!-- TIÊU ĐỀ -->
            <div class="text-center">
                <h2
                    class="text-2xl md:text-3xl font-bold text-black relative inline-block"
                >
                    <span class="px-4">XU HƯỚNG TÌM KIẾM</span>
                    <div
                        class="absolute left-0 right-0 top-1/2 transform -translate-y-1/2 border-t border-gray-400 z-[-1]"
                    ></div>
                </h2>
            </div>

            <!-- DANH MỤC -->
            <div
                class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-6 gap-6 text-center"
            >
                <div
                    v-for="(trend, index) in trends"
                    :key="index"
                    class="space-y-2"
                >
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
        image: "images/trend_vong.png",
    },
    {
        label: "NHẪN",
        image: "images/trend_nhan.png",
    },
    {
        label: "DÂY CHUYỀN",
        image: "images/trend_day.png",
    },
    {
        label: "BÔNG TAI",
        image: "images/trend_bongtai.png",
    },
    {
        label: "CHARM PANDORA",
        image: "images/trend_charm.png",
    },
    {
        label: "KHUYÊN XỎ",
        image: "images/trend_khuyen.png",
    },
];
</script>

<style scoped>
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css");
</style>
