<template>
  <section>
    <friend-nav></friend-nav>
    <friend-form></friend-form>
    <friend-card></friend-card>
  </section>
</template>

<script>
import FriendNav from './components/FriendNav.vue'
import FriendForm from './components/FriendForm.vue'
import FriendCard from './components/FriendCard.vue'

export default {
  name: 'App',
  components: {
    FriendNav,
    FriendForm,
    FriendCard
  },
  data() {
    return {
      
    }
  }
}
</script>

<style>
  * {
    margin: 0;
  }

</style>
