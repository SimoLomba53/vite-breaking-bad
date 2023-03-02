<script>

import SingleCard from './SingleCard.vue';

export default {

    props: { cards: Array },


    components: { SingleCard },

};


</script>

<template>
         <div class="card-conteiner">
          <SingleCard v-for="card in cards" :type="card.archetype" :form="card.type"  :name="card.name"  :pic="card.card_images"/>
         </div>
    
</template>

<style scoped>


</style>
