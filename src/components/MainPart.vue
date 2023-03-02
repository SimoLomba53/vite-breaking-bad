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
       <div class="input-group mb-3">
         <input type="text" class="form-control" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="basic-addon2">
         <button>RESEND</button>
        </div>
      <div>
        <li>
          <CardList :cards="cards" />
        </li>
      </div>
    </div>
  </section>
</template>

<style scoped></style>
