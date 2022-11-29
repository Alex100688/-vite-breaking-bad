<script>
    export default {
        name: "CardCharacters",
        props: {
            info:Object,
        },
    }
</script>
<template>
    <div class="text-center">
        <img  :src="info.img" :alt="info.name">
        <h6>{{info.name}}</h6>
        <div>{{info.category}}</div>
        <div>{{info.status}}</div>
        
        
    </div>
</template>


<style lang="scss" scoped>
    img{
        width: 9.375rem;
        height: 12.5rem;
        object-fit: cover;
    }
</style>