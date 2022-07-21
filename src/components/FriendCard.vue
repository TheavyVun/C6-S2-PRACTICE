<template>
    <section>
        <h2>{{fullname}}</h2>
        <p>{{friend.comment}}</p>
        <label for="">Skills: </label>
        <ul> 
          <friend-skill v-for="skill of friend.skill" :key="skill" :skill="skill" />
        </ul>
    </section>
</template>

<script>
import Skill from './FriendSkill.vue'
export default {
  components: {
    'friend-skill': Skill,
  },
  props: {
    friend: Object,
  },
  computed: {
    fullname() {
        return this.friend.firstname + ' ' + this.friend.lastname;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    section {
        width: 40%;
        margin: auto;
        padding: 20px;
        border-radius: 10px;
        margin-top: 15px;
        box-shadow: 0 2px 8px rgba(34, 32, 32, 0.26);
        background: rgb(214, 210, 210);
        border-top: 4px solid rgb(189, 46, 46);
    }
    p {
        margin-top: 10px;
    }
    ul {
        margin: 0;
        box-sizing: border-box;
        width: 90%;
    }
</style>