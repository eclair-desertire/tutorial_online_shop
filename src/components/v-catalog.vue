<template>
    <div class="v-catalog">
        <h1>Catalog</h1>
        <vCatalogItem 
            v-for="product in PRODUCTS"
            :key="product.id"
            :product="product"
            @sendDataToParent="sendFromChild"
        />
    </div>
</template>

<script>
import vCatalogItem from './v-catalog-item.vue';
import { mapActions, mapGetters } from 'vuex';

export default{
    name: "v-catalog",
    components:{
        vCatalogItem
    },
    data(){
        return{
            
        }
    },
    computed:{
        ...mapGetters([
            'PRODUCTS'
        ]),
    },
    methods:{
        ...mapActions([
            'GET_PRODUCTS_FROM_API'
        ]),
        sendFromChild(data){
            console.log(data)
        }
    },
    mounted(){
        this.GET_PRODUCTS_FROM_API();
    }
}
</script>

<style lang="scss">
.v-catalog{
    &__list{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        align-items: center;
    }
}
</style>