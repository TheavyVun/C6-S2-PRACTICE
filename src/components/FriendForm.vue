<template>
    <form @submit.prevent="addfriend" action="#">
        <input v-model="firstname" type="text" placeholder="First Name" class="form-control">
        <input v-model="lastname" type="text" placeholder="Last Name" class="form-control">
        <input v-model="comment" type="text" placeholder="Comment" class="form-control">
         <div> Skills: 
            <input type="checkbox" name="skills" id="1" value="HTML" v-model="checkskill">
            <label for="1">HTML</label>
            <input type="checkbox" name="skills" id="2" value="CSS" v-model="checkskill">
            <label for="2">CSS</label>
            <input type="checkbox" name="skills" id="3" value="PHP" v-model="checkskill">
            <label for="3">PHP</label>
            <input type="checkbox" name="skills" id="3" value="VUE" v-model="checkskill">
            <label for="4">VUE</label>
        </div>
        <button @add-friend="addfriend" class="form-control btn" type="submit">ADD</button>
    </form>
</template>

<script>
export default {
    emits: ["add-friend"],
    data() {
        return {
            firstname: '',
            lastname: '',
            comment: '',
            checkskill: [],
        }
    },
    methods: {
        addfriend(e) {
            e.preventDefault
            if (this.firstname != '' && this.lastname != '' && this.comment != '') {
                let friend = {
                    firstname: this.firstname,
                    lastname: this.lastname,
                    comment: this.comment,
                    skill: this.checkskill,
                }
                this.$emit('add-friend', friend);
                this.firstname = '';
                this.lastname = '';
                this.comment = '';
                this.checkskill = [];

            }

        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    form {
        width: 40%;
        padding: 20px;
        border-radius: 10px;
        margin: auto;
        margin-top: 20px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);

    }
    .form-control {
        width: 100%;
        box-sizing: border-box;
        padding: 10px;
        margin-bottom: 16px;
        border: solid 1px rgb(124, 117, 117);
        border-radius: 5px;
        outline: none;
    }
    .btn {
        background: rgb(156, 139, 139);
        border: none;
        color: #fff;
    }
    .btn:hover {
        background: rgb(176, 33, 33);
    }
</style>