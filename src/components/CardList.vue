<script>
import BaseSearch from './BaseSearch.vue';
import SingleCard from './SingleCard.vue';

export default {


    props: { cards: Array },
   

    components: { SingleCard, BaseSearch },
     

    methods:{ 

    searchingFilter(term) {
        console.log(term);
    },
    },

 
};


</script>

<template>

        <BaseSearch  @searching="searchingFilter"  />        

         <div class="card-conteiner">
          <SingleCard v-for="card in cards" :type="card.archetype" :form="card.type"  :name="card.name"  :pic="card.card_images"/>
         </div>
    
</template>

<style scoped>


</style>
