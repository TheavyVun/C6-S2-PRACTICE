<template>
    <li>{{skill}}</li>
</template>

<script>
export default {
  props: {
    skill: String,
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    li {
        list-style: none;
        box-shadow: 0 2px 8px rgba(34, 32, 32, 0.26);

        padding: 10px 20px;
        margin: 2px;
    }
</style>