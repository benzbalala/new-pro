<template>
    <div id="container">
        <div id="comment-container">
            <h1>เเสดงความคิดเห็น</h1>
            <div class="comment" v-for="(comment, index) in comments" :key="index">
                <img src="../../assets/1.png">
                <div class="comment-right">
                    <h3>{{ comment.name }}</h3>
                    <p id="date">{{ comment.date }}</p>
                    <p id="comment-text">{{ comment.commentText }}</p>
                </div>
            </div>
        </div>

    </div>
</template>
<script>
export default {
    data() {
        return {
            comments: [
                {
                    name: 'คนค้นคน 1',
                    date: '2020-11-11 | สีฟ้า, ไซส์ L',
                    commentText: 'รอบแรกซื้อมา 1 ตัว เพราะจะลองเนื้อผ้าก่อน รอบนี้ซื้อรอบที่ 2 แล้ว จัดไป 4 ตัวเลย ใส่สบาย ผ้านิ่ม สีสวย ดูระบายอากาศและไม่บาง คุ้มกับราคามากๆ ค่ะ ทางร้านส่งของให้ไวไม่ช้า ไว้จะสั่งอีกแน่นอนค่ะ',
                },
                {
                    name: 'คนค้นคน 2',
                    date: '2021-01-15 | สีแดง, ไซส์ M',
                    commentText: 'ขอบคุณทางร้านที่จัดส่งสินค้าอย่างรวดเร็ว ผ้ามาตรฐานดี สวมใส่สบายมาก ขอบคุณมากค่ะ!',
                },
                {
                    name: 'คนค้นคน 3',
                    date: '2022-03-22 | สีเหลือง, ไซส์ XL',
                    commentText: 'สินค้าคุณภาพดีมาก ราคาถูก ผ้านุ่ม สวมใส่สบายมาก ห้างร้านจัดส่งรวดเร็วมากค่ะ',
                },
            ],
        };
    },
};
</script>
<style scoped>
#container {
    display: flex;
    width: 100vw;
    flex-direction: column;
    align-items: center;
}

#comment-container {
    width: 1200px;
    /* margin-right: 60px; */
    background-color: rgb(255, 255, 255);
    margin-bottom: 30px;
    padding: 20px 50px 20px 50px;
}

.comment {
    background-color: rgb(234, 240, 238);
    display: flex;
    width: 100%;
    height: 120px;
    margin-top: 10px;
    align-items: center;
}

.comment img {
    height: 65px;
    width: 65px;
    border-radius: 40px;
    margin: 0 20px 0 20px;
}

.comment-right {
    display: flex;
    flex-direction: column;
    /* gap: 0.5rem; */
}
.comment-right p {
    margin: 0;
}
.comment-right h3 {
    margin: 0;
}
#comment-text {
    font-size: 16px;
}

#date {
    font-size: 12px;
    color: rgb(87, 86, 86);
}
</style>