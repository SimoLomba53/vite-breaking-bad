<script>
import CardList from './CardList.vue';

export default {


  components: { CardList },
}


</script>

<template>
  <section>
    <div>
      <div>
        <li>
          <CardList v-for="card in cards" />
        </li>
      </div>
    </div>
  </section>
</template>

<style scoped></style>
