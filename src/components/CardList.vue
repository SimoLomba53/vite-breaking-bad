<script>

import SingleCard from './SingleCard.vue';

export default {

    props: { cards: Object },


    components: { SingleCard },

};


</script>

<template>
    <div>
        <SingleCard v-for="card in cards" :type="card.archetype"/>
    </div>
</template>

<style scoped></style>
