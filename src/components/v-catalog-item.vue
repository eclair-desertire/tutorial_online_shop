<template>
    <div class="v-catalog-item">
        <h1>{{product.title}}</h1>
        <h2>{{product.category}}</h2>
        <img :src="product.image" style="width: 100%;" alt="">
        <h2>Price: {{product.price}}</h2>
        <p>{{product.description}}</p>
        <button>Add to Cart</button>
    </div>
</template>

<script>


export default{
    name: "v-catalog-item",

    props:{
        product: {
            type: Object,
            default() {
                return {}
            }
        },
    },
    data(){
        return{}
    },
    computed:{}
}
</script>

<style lang="scss">
.v-catalog-item{
    flex-basis: 25%;
    box-shadow: 0 0 8px 0 #e0e0e0;
    padding: 16px;
    margin-bottom: 16px;
}
</style>