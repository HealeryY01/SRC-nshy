<template>
    <section class="product-list">
        <h2 class="text-center text-danger font-weight-bold">
            Các sản phẩm nổi bật
        </h2>
        <div class="pro-list row ">
            <div v-for="(productItem, index) in productList" :key="index" class="col-lg-3">
                <product-item :productItem="productItem" @hanlde-buy="hanldeBuy" />
            </div>
        </div>
    </section>
</template>
<script>
import ProductItem from "./ProductItem.vue";
import sp1 from "../assets/images/nhan-long.jpg";
import sp2 from "../assets/images/gao-nep.jpg";
import sp3 from "../assets/images/gao-st25.jpg";
import sp4 from "../assets/images/bot-san-day.jpg";
import sp5 from "../assets/images/hat-sen.jpg";
import sp6 from "../assets/images/mat-ong-long-nhan.jpg";
import sp7 from "../assets/images/long-nhan.jpg";
import sp8 from "../assets/images/tuong-ban.jpg";
export default {
    components: {
        ProductItem,
    },
    data() {
        return {
            productList: [
                {
                    id: 1,
                    name: "Nhãn Lồng",
                    image: sp1,
                    description: "Nhãn lồng Hưng Yên có vỏ màu vàng sậm tự nhiên, cùi giòn, hạt nhỏ đen nháy, mùi thơm tự nhiên, đáy có hai dẻ cùi lồng xếp khít vào nhau. Quả nhãn lồng hưng yên có hình tròn, vỏ ngoài màu vàng xám, hầu như nhẵn. Hạt nhãn đen nhánh, có lớp lụa mỏng màu trắng bao bọc.",
                    price: 180000,
                    sale: 10,
                    quantityInStock: 10,
                },
                {
                    id: 2,
                    name: "Gạo Nếp Thơm",
                    image: sp2,
                    description: "Nếp thơm Hưng Yên là giống cảm ôn, thuộc nhóm ngắn ngày có thời gian sinh trưởng 125 - 130 ngày trong vụ Xuân và 105-110 ngày vụ Mùa (Hè thu) tại các tỉnh phía Bắc. Nếp thơm Hưng Yên có chiều cao cây 105-110 cm, số hạt/bông 140-160 hạt/bông, tỷ lệ hạt lép thấp (10-15%), khối lượng 1.000 hạt: 29-30 gram.",
                    price: 250000,
                    sale: 5,
                    quantityInStock: 15,
                },
                {
                    id: 3,
                    name: "Gạo ST-25",
                    image: sp3,
                    description: "Gạo ST25 là một giống gạo cao cấp của Việt Nam, được phát triển bởi Học viện Nông nghiệp Việt Nam phối hợp với Công ty TNHH Giống cây trồng Tây Đô. Đây là một giống gạo mới, được ra đời từ quá trình lai tạo giữa hai giống gạo là gạo Vĩnh Hưng và gạo ĐBSCL.Gạo ST25 có hạt gạo dài, thon, mềm, vị ngọt đậm đà, thơm mùi dừa và có độ đậm đặc, độ bóng cao.",
                    price: 250000,
                    sale: 0,
                    quantityInStock: 5,
                },
                {
                    id: 4,
                    name: "Bột Sắn Dây",
                    image: sp4,
                    description: "Bột sắn dây được làm từ củ của cây sắn dây (còn được gọi là cát căn, cam cát căn theo Đông Y). Bột sắn dây có màu trắng và thường ở dạng bột rắn. Bạn chú ý phân biệt bột sắn dây với bột năng, thường nhầm lẫn do tên gọi vùng miền. Bột năng được làm từ củ sắn hay còn gọi là củ mì. Tuy nhiên 2 loại này cũng rất dễ phân biệt vì bột năng ở dạng bột mịn khác với dạng bột sắn dây ở trên.",
                    price: 120000,
                    sale: 5,
                    quantityInStock: 35,
                },
                {
                    id: 5,
                    name: "Hạt sen Khô",
                    image: sp5,
                    description: "Hạt sen khô Hưng Yên là thành phẩm được sơ chế từ 100% hạt sen trồng, canh tác tại các tỉnh Hưng Yên, Hà Nam, Thái Bình,… Hạt sen già sau khi thu hoạch sẽ được phơi, sấy khô, chặt vỏ, trà vỏ lụa (màng hồng) bên ngoài, thông tâm sen và sấy khô để bảo quản.",
                    price: 150000,
                    sale: 5,
                    quantityInStock: 50,
                },
                {
                    id: 6,
                    name: "Mật Ong Nhãn",
                    image: sp6,
                    description: "Mật ong nhãn nguyên chất là loại mật ong phổ biến, được thu hoạch từ vùng nhãn lồng trứ danh Phố Hiến Hưng Yên. Mật có màu nâu vàng, mùi thơm dịu, vị ngọt thanh khiết của nhãn, thích hợp để nấu ăn, pha trà, mang đến món quà sức khỏe cho mọi lứa tuổi.",
                    price: 110000,
                    sale: 0,
                    quantityInStock: 100,
                },
                {
                    id: 7,
                    name: "Tương bần ",
                    image: sp8,
                    description: "Còn tương Bần vốn là đặc sản của thị trấn Bần Yên Nhân (Mỹ Hào). Nghề làm tương Bần có cách đây gần 10 thế kỷ, nổi tiếng là loại nước chấm thơm ngon độc đáo. Hiện nay, làng nghề sản xuất tương Bần có 20 cơ sở sản xuất qui mô lớn, mỗi năm sản xuất ra thị trường trên 10 triệu lít.",
                    price: 90000,
                    sale: 5,
                    quantityInStock: 120,
                },
                {
                    id: 8,
                    name: "Long nhãn",
                    image: sp7,
                    description: "Long nhãn Hưng Yên có mùi thơm nhẹ đặc trưng, vị ngọt bùi, mềm dẻo, mặt ngoài nhăn mặt trong láng mịn. Không chỉ được ưa chuộng sử dụng trong đời sống hàng ngày, long nhãn còn chứa rất nhiều dưỡng chất và là một vị thuốc có nguồn gốc từ tự nhiên giúp bảo vệ sức khỏe, chữa trị nhiều bệnh khác nhau.",
                    price: 110000,
                    sale: 5,
                    quantityInStock: 65,
                },
            ],
        };
    },
    methods: {
        hanldeBuy(productItem) {
            console.log(productItem);
            this.$emit('hanlde-buy', productItem);
        }
    }
};
</script>
<style></style>