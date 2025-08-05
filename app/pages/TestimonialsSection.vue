<template>
    <section class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4">
            <!-- Tiêu đề -->
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-bold text-red-500">
                    Cảm Nhận Khách Hàng Về Chương Trình Đào Tạo
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
        text: "Trước đây mình ngại makeup, nhưng học tại PLITA giúp mình biết cách trang điểm nhẹ nhàng mỗi ngày, tự tin hơn khi đi làm và gặp khách hàng.",
        name: "Tuyết Nguyễn",
        avatar: "images/avt_1.png",
        verified: true,
    },
    {
        text: " Mình từng làm công việc văn phòng nhưng không tìm thấy đam mê. Sau khóa học tại PLITA, mình đã có tay nghề cơ bản, tự tin nhận khách makeup đi tiệc. Lộ trình rõ ràng, thực hành nhiều, giảng viên tận tâm – mình thấy đây là quyết định đúng đắn nhất!",
        name: "Béo Chy",
        avatar: "images/avt_2.png",
        verified: false,
    },
    {
        text: "Là người chia sẻ về làm đẹp, mình luôn muốn học bài bản để nâng tầm kiến thức. Tại PLITA, mình được học từ nền tảng đến chuyên sâu, hiểu đúng kỹ thuật và cách truyền cảm hứng cho người khác. Đây là nơi mình phát triển nghề và thương hiệu cá nhân!",
        name: "Bao Huỳnh",
        avatar: "images/avt_3.png",
        verified: true,
    },
];
</script>

<style scoped>
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css");
</style>
