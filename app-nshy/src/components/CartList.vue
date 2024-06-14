<template>
    <table class="table">
        <thead>
            <tr>
                <th>STT</th>
                <th>Tên</th>
                <th>Giá</th>
                <th>Số Lượng Trong Kho</th>
                <th>Số Lượng</th>
                <th>Thành tiền</th>
                <th>Hành Động</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(cart, index) in cartList" :key="index">
                <td scope="row">{{ index + 1 }}</td>
                <td>{{ cart.name }}</td>
                <td>{{ cart.price }}</td>
                <td>{{ cart.quantityInStock }}</td>
                <td>
                    <button class="btn btn-success"><i class="fa fa-arrow-up"></i></button>
                    <span class="mx-2">1</span>
                    <button class="btn btn-success"><i class="fa fa-arrow-down"></i></button>
                </td>
                <td>0</td>
                <td>
                    <button class="btn btn-danger">
                        <i class="fa fa-trash"></i>
                    </button>
                </td>
            </tr>
        </tbody>
    </table>
</template>
<script>
export default {
    props: {
        cartList: {
            type: Array,
        }
    },
};
</script>