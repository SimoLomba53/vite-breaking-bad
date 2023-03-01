<script>

import SingleCard from './SingleCard.vue';

export default {
    components: { SingleCard },
    props: { cards: Array },
}


</script>

<template>
    <div>
        <SingleCard v-for="card in cards" />
    </div>
</template>

<style scoped></style>
