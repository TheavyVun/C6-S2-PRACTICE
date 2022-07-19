<template>
    <form action="">
        <input type="text" placeholder="First Name" class="form-control">
        <input type="text" placeholder="Last Name" class="form-control">
        <input type="text" placeholder="Comment" class="form-control">
        <button class="form-control btn" type="submit">ADD</button>
    </form>
</template>

<script>
export default {
    name: 'friend-form',
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