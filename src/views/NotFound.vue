<template>
  <div>
    <h1>Oh, it's not here.</h1>
    <h3>This is not the {{ resource }} you are looking for.</h3>
    <router-link :to="{ name: 'event-list' }">Take me back</router-link>
  </div>
</template>

<script>
export default {
  props: {
    resource: {
      type: String,
      required: true
    }
  }
}
</script>
