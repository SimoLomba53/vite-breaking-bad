<script>
import CardList from './CardList.vue';

export default {
  props: { cards: Array },

  components: { CardList },
}


</script>

<template>
  <section>
    <div>
      <div>
        <li>
          <CardList :cards="cards" />
        </li>
      </div>
    </div>
  </section>
</template>

<style scoped></style>
