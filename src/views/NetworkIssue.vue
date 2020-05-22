<template>
  <div>
    <h1>Oh, it's not working</h1>
    <h3>
      You might have a network issue, please click the back button and try again
    </h3>
    <router-link :to="{ name: 'event-list' }">Take me back</router-link>
  </div>
</template>

<script>
export default {}
</script>

<style></style>
