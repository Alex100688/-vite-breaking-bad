<script>
import AppCharachters from './AppCharachters.vue';
    export default {
    name: "AppMain",
    components: {
        AppCharachters
    },
       
    }
</script>
<template>
    <div class="container mt-auto ">
        <select class="form-select-sm my-3" >
        <option selected>Select Category</option>
        <option value="1">Name</option>
        <option value="2">Occupation</option>
        <option value="3">Status</option>
      </select>
    </div>
    <div class="container container-main mt-auto">
        <div class="col-12 py-2 color-found">
            <h6>Found 62 charachters</h6>
        </div>
    </div>
    <AppCharachters/>
</template>


<style lang="scss" scoped>
    select{
        border: none;
    }
    .container-main{
        background-color: white;
    }
    .color-found{
        background-color: #212529;
        h6{
            color: white;
        }
    }
</style>