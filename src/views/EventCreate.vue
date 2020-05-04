<template>
  <div>
    <h1>Create Event, {{ user.name }}</h1>
    <p>This event was created by {{ user.id }}</p>
    <p>There are {{ catLength }} categories</p>
    <ul>
      <li v-for="cat in categories" :key="cat">{{ cat }}</li>
    </ul>
    <p>{{ getEvent(1) }}</p>
    <p>{{ getEventById(3) }}</p>
  </div>
</template>

<script>
import { mapState, mapGetters} from 'vuex'

export default {
  computed: {
    getEvent() {
      return this.$store.getters.getEventById
    },
    catLength() {
      return this.$store.getters.catLength
    },
    ...mapState(['user', 'categories']),
    ...mapGetters(['getEventById'])
  }
}
</script>

<style></style>
