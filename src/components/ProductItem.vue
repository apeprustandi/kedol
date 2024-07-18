<template>
    <div class="product-item">
        <img :src="`https://api.cibinong.online${product.imageUrl}`" alt="">
        <h3 class="product-name">{{ product.name }}</h3>
        <p class="product-price">Rp{{ product.price }}</p>
        <router-link :to="{ name: 'product-detail', params: {id: product.code} }">
            <button>Detail</button>
        </router-link>
    </div>
</template>

<script>
export default {
    props: [
        'product'
    ]
}
</script>

<style scoped>
.product-item {
    align-items: center;
    border-radius: 8px;
    box-shadow: 0px 2px 5px #888;
    display: flex;
    flex-direction: column;
    margin-bottom: 2%;
    padding: 20px;
    position: relative;
    width: 100%;
    max-width: 300px;
    margin: 1rem auto;
}

.product-name {
    margin-bottom: 0;
}

img {
    height: auto;
    width: 100%;
    max-width: 200px;
    border-radius: 5%;
}

a {
    width: 100%;
}

button {
    width: 100%;
}

@media (max-width: 767px) {
    .product-item {
        width: 100%;
    }
}

@media (min-width: 768px) {
    .product-item {
        width: 48%;
    }
}

@media (min-width: 1024px) {
    .product-item {
        width: 32%;
    }
}
</style>
