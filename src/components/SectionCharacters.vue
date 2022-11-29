<script>
import axios from "axios";
import CardCharcaters from './CardCharcaters.vue';
export default
    {
        name: "SectionCharacters", 
        components: {
            CardCharcaters,
        },
        data() {
            return {
                characters: []
            }
        },
       created () {
           axios.get("https://www.breakingbadapi.com/api/characters")
               .then((figures) => {
                   this.characters = figures.data;

               });
       },
    }
</script>
<template>
    <section class="container">
        <div class="row justify-content-center ">
            <CardCharcaters class="col-2"/>
            <CardCharcaters class="col-2"/>
            <CardCharcaters class="col-2"/>
            <CardCharcaters class="col-2"/>
            <CardCharcaters class="col-2"/>



        </div>
    </section>
        
</template>


<style lang="scss" scoped>
   
</style>