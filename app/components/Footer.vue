<template>
    <footer
        class="bg-pink-50 text-gray-700 pt-10 pb-6 border-t border-pink-200"
    >
        <div
            class="max-w-7xl mx-auto px-4 grid grid-cols-1 md:grid-cols-4 gap-8"
        >
            <!-- Logo và mô tả -->
            <div>
                <NuxtLink to="/" class="flex items-center space-x-2 mb-4">
                    <img
                        src="/images/avt_1.png"
                        alt="Logo"
                        class="h-10 w-auto"
                    />
                    <span class="font-bold text-pink-600 text-lg"
                        >Phú Giáo Jewelry</span
                    >
                </NuxtLink>
                <p class="text-sm">
                    Cửa hàng trang sức uy tín với hàng trăm mẫu mã đa dạng, tinh
                    tế và giá cả hợp lý dành cho mọi lứa tuổi.
                </p>
            </div>

            <!-- Danh mục -->
            <div>
                <h4 class="text-pink-600 font-semibold mb-3">Danh mục</h4>
                <ul class="space-y-2 text-sm">
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-500"
                            >Trang chủ</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-500"
                            >Sản phẩm</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-500"
                            >Khuyến mãi</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-500"
                            >Liên hệ</NuxtLink
                        >
                    </li>
                </ul>
            </div>

            <!-- Hỗ trợ -->
            <div>
                <h4 class="text-pink-600 font-semibold mb-3">
                    Hỗ trợ khách hàng
                </h4>
                <ul class="space-y-2 text-sm">
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-500"
                            >Chính sách đổi trả</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-500"
                            >Chính sách bảo hành</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-500"
                            >Giao hàng & Thanh toán</NuxtLink
                        >
                    </li>
                    <li>
                        <NuxtLink to="/" class="hover:text-pink-500"
                            >Hướng dẫn mua hàng</NuxtLink
                        >
                    </li>
                </ul>
            </div>

            <!-- Liên hệ -->
            <div>
                <h4 class="text-pink-600 font-semibold mb-3">Liên hệ</h4>
                <ul class="space-y-2 text-sm">
                    <li>
                        <i class="fas fa-map-marker-alt mr-2 text-pink-400"></i
                        >Phước Hòa, Phú Giáo, Bình Dương
                    </li>
                    <li>
                        <i class="fas fa-phone mr-2 text-pink-400"></i>0937 704
                        598
                    </li>
                    <li>
                        <i class="fas fa-envelope mr-2 text-pink-400"></i
                        >tanthanh1998.phuochoa@go2joy.vn
                    </li>
                    <li class="flex space-x-3 mt-2">
                        <a href="#" class="text-pink-500 hover:text-pink-700"
                            ><i class="fab fa-facebook-f"></i
                        ></a>
                        <a href="#" class="text-pink-500 hover:text-pink-700"
                            ><i class="fab fa-instagram"></i
                        ></a>
                        <a href="#" class="text-pink-500 hover:text-pink-700"
                            ><i class="fab fa-tiktok"></i
                        ></a>
                        <a href="#" class="text-pink-500 hover:text-pink-700"
                            ><i class="fab fa-youtube"></i
                        ></a>
                    </li>
                </ul>
            </div>
        </div>

        <!-- Bản quyền -->
        <div
            class="text-center text-xs mt-8 text-gray-500 border-t border-pink-100 pt-4"
        >
            © 2025 Phú Giáo Jewelry. Đã đăng ký bản quyền.
        </div>
    </footer>
</template>

<script setup>
// Không cần logic
</script>

<style scoped>
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css");
</style>
