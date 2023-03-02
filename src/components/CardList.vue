<script>

import SingleCard from './SingleCard.vue';

export default {

    props: { cards: Array },


    components: { SingleCard },

};


</script>

<template>
         <div>
          <SingleCard v-for="card in cards" :type="card.archetype"  :name="card.name"  :pic="card.card_images"/>
         </div>
    
</template>

<style scoped></style>
