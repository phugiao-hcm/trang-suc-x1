<template>
    <section class="py-12 bg-white">
        <div class="max-w-7xl mx-auto px-4">
            <!-- Tiêu đề -->
            <div class="text-center mb-10">
                <h2
                    class="text-2xl md:text-3xl font-bold text-black relative inline-block"
                >
                    <span class="px-4">SẢN PHẨM YÊU THÍCH NHẤT</span>
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
                            <span class="text-gray-500 text-xs">{{
                                product.code
                            }}</span>
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
                                :class="`w-4 h-4 rounded border border-gray-300`"
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
        name: "Dây chuyền bạc nữ đính đá CZ cá tiên",
        code: "LILI_831944",
        price: "1.023.000₫",
        image: "images/love_1.png",
    },
    {
        name: "Nhẫn bạc nữ đính kim cương Moissanite Aidan",
        code: "LILI_335168",
        price: "1.475.000₫",
        image: "images/love_2.png",
    },
    {
        name: "Lắc chân bạc nữ đính đá CZ hình cỏ 4 lá Mildred",
        code: "LILI_763298",
        price: "1.014.000₫",
        image: "images/love_3.png",
    },
    {
        name: "Dây chuyền đôi bạc tình yêu BFF đính đá CZ Forever Love",
        code: "LILI_528145",
        price: "2.098.000₫",
        image: "images/love_4.png",
    },
    {
        name: "Nhẫn cặp đôi bạc đính kim cương Moissanite Theophilus",
        code: "LILI_672438",
        price: "1.751.000₫",
        image: "images/love_5.png",
    },
    {
        name: "Bông tai bạc nữ đính đá CZ có 4 lá",
        code: "LILI_453329",
        price: "726.000₫ – 759.000₫",
        image: "images/love_6.png",
        colors: ["#ccc", "#e91e63", "#2196f3"],
    },
    {
        name: "Lắc tay bạc nữ đính pha lê Swarovski trái tim biển",
        code: "LILI_579467",
        price: "1.139.000₫",
        image: "images/love_7.png",
        colors: ["#f50057", "#3f51b5", "#00bcd4"],
    },
    {
        name: "Lắc tay bạc nam mắt xích Cuban Saint Laurent Paris",
        code: "LILI_746785",
        price: "4.116.000₫ – 5.299.000₫",
        image: "images/love_8.png",
    },
];
</script>
