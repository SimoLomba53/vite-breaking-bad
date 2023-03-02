<script>
import BaseSearch from './BaseSearch.vue';
import SingleCard from './SingleCard.vue';

export default {
    

    data(){
        return{
            endpoint: "https://db.ygoprodeck.com/api/v7/cardinfo"
        }
    },
     
    props: { cards: Array },
   

    components: { SingleCard, BaseSearch },
     

    methods:{ 

    cardcharacters(response){
        console.log(response);
    },

    searchingFilter(term) {
        console.log(term);

        this.cardcharacters(`${this.endpoint}?form=${term}`);
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
