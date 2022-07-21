<template>
  <section>
    <friend-nav />
    <friend-form @add-friend="addFriend" />
    <friend-card v-for="friend of friends" :key="friend" :friend="friend" />
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
    FriendCard,
  },
  data() {
    return {
      friends: [
        {firstname: "Theavy", lastname: "Vun", comment: "The best Player of the team🤣😂", skill: ["HTML", "CSS", "PHP", "VUE"]},
        {firstname: "Theavy", lastname: "Vun", comment: "The best Player of the team🤣😂", skill: ["HTML", "CSS", "PHP", "VUE"]},
        {firstname: "Theavy", lastname: "Vun", comment: "The best Player of the team🤣😂", skill: ["HTML", "CSS", "PHP", "VUE"]},
      ],

    }
  },
  methods: {
    addFriend(friend) {
      this.friends.push(friend);
    }
  }

}
</script>

<style>
  * {
    margin: 0;
  }

</style>
