<template>
    <div class="v-main-wrapper">
        <p>{{title}}</p>
        <vCart/>
        <vCatalog/>

    </div>
</template>

<script>
import vCatalog from './v-catalog.vue';

import vCart from './v-cart.vue';

export default{
    name: "v-main-wrapper",
    components:{
        vCatalog,
        vCart
    },
    props:{},
    data(){
        return {
            title:"Main Wrapper title"
        }
    },
    computed:{
        
    },
    methods:{

    },
    watch:{

    },
    mounted(){
        console.log('v-main-wrapper mounted')
    },

}
</script>

<style>
    .v-main-wrapper{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        max-width: 900px;
        margin: 0 auto;
    }
</style>