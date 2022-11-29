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
        <div class="row g-3 justify-content-center ">
            <CardCharcaters v-for="character in characters" class="col-2" :info="character"/>
            
            



        </div>
    </section>
        
</template>


<style lang="scss" scoped>
   
</style>