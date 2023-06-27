<template>
    <div class="product">
        <h3>{{ product.name }}</h3>
        <h3 class="price">{{ formattedPrice }}</h3>
        <p v-if="product.available">Available</p>
        <p v-else>Out of stock</p>

    </div>
</template>

<script>
export default {
    name: 'ProductDetails',

    data() {
        return {
            product: {
                name: "Монитор Samsung",
                price: 169.99,
                available: true,
            }
        };
    },

    computed: {
        formattedPrice: function () {
            return `$ ${this.product.price}`;
        }
    },

    methods: {

    },
};
</script>

<style lang="css" scoped>
.product {
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 1px solid black;
    border-radius: 10px;
    width: 250px;
    background-color: yellow;
}

.price {
    color: red;
}
</style>