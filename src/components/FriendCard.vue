<template>
    <section v-for="friend of friends" :key="friend.id">
        <h2>{{friend.firstname}} {{friend.lastname}} </h2>
        <p>{{friend.comment}}</p>
    </section>
</template>

<script>
export default {
    data() {
        return {
            friends: [
            {id: 1, firstname: "RONAN", lastname: "OGOR", comment: "The best of the best"},
            {id: 2, firstname: "RONAN", lastname: "OGOR", comment: "The best of the best"},
            {id: 2, firstname: "RONAN", lastname: "OGOR", comment: "The best of the best"},
            ],
        }
    },

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
</style>