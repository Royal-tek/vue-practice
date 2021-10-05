<template>
<div class="card">
    <h3 class="name">{{product.name}}</h3>
    <h5 class = "price">Price: ${{product.price}}</h5>
    <p class="description">{{description}}</p>
    <p class="text-muted">{{product.category}}</p>
    <button class="view-product-button" @click="$emit('view-product',product)">View</button>
    
    
</div>

</template>

<script>
export default {
    name : 'productsummarycard',
    props : ['product'],
    computed :{
        description(){
            return this.product.description.substring(0,100)
        }
    },
}
</script>
<style lang="scss">
    .card{
        width: 80%;
        padding:10px;
        margin:10%;
        border-radius : 5px;
        background-color:white;
        // display: flex;
        // flex-direction : column;
        // justify-content: center;
        // align-items: center;
        box-shadow : 0 0 5px gray;

    h5.price{
        color: gray;
    }
    p.description{
        font-size: .85rem;
    }
    p.text-muted{
        color: gray;
    }
    button.view-product-button{
        background-color: rgb(79, 160, 187);
        border: none;
        color: white;
        font-weight: bold;
        font-size: 1.15rem;
        border-radius: 5px;
        cursor: pointer;
        padding: 10px;
    }
    button.view-product-button:hover{
        background-color: rgb(8, 71, 92);
        color: white;
        transition: 1s;
    }
    }
    @media (min-width:500px){
        .card{
            width:350px;
            margin: 10px;
        }
    }
    
</style>