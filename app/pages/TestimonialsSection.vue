<template>
    <section class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4">
            <!-- Tiêu đề -->
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-bold text-red-500">
                    Cảm Nhận Khách Hàng khi mua Trang Sức
                </h2>
                <div class="mt-2 w-20 h-1 bg-red-500 mx-auto"></div>
            </div>

            <!-- Danh sách đánh giá -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div
                    v-for="(feedback, index) in feedbacks"
                    :key="index"
                    class="bg-white p-6 rounded-2xl shadow-sm border text-gray-700 space-y-4"
                >
                    <!-- Nội dung -->
                    <p>{{ feedback.text }}</p>

                    <!-- Rating -->
                    <div class="text-red-500 text-sm">
                        <span v-for="i in 5" :key="i">
                            <i class="fas fa-star"></i>
                        </span>
                    </div>

                    <!-- Người dùng -->
                    <div class="flex items-center gap-3 pt-2">
                        <img
                            :src="feedback.avatar"
                            alt="avatar"
                            class="w-10 h-10 rounded-full object-cover"
                        />
                        <div
                            class="text-sm font-bold text-red-500 flex items-center gap-1"
                        >
                            {{ feedback.name }}
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
const feedbacks = [
    {
        text: "Vừa nhận được món trang sức, phải nói là xinh hơn cả mong đợi!. Thiết kế tinh tế, đeo lên nhìn cực kỳ sang và cuốn hút. Rất ưng ý, chắc chắn sẽ ủng hộ thêm lần sau! 💖",
        name: "Tuyết Nguyễn",
        avatar: "images/avt_1.png",
        verified: true,
    },
    {
        text: "Món trang sức này đúng chuẩn “yêu từ cái nhìn đầu tiên”!. Vừa nhẹ, vừa sáng, lại hợp gu mình quá trời luôn. Cảm ơn shop vì sản phẩm và dịch vụ tuyệt vời nha! ✨",
        name: "Béo Chy",
        avatar: "images/avt_2.png",
        verified: false,
    },
    {
        text: "Mình đã đeo thử và nhận được rất nhiều lời khen. Trang sức đẹp, chất lượng tốt, cực kỳ phù hợp đi tiệc hay chụp hình. Không ngờ giá lại quá “mềm” so với vẻ ngoài sang chảnh như vậy!",
        name: "Bao Huỳnh",
        avatar: "images/avt_3.png",
        verified: true,
    },
];
</script>

<style scoped>
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css");
</style>
