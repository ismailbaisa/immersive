<template>
<div class="content">
    <div class="card">
        <div><img class="avatar" src="https://i.imgur.com/BoYTeCZ.png"></div>
        <div class="card-content">
            <div>
                <b>Name</b>
                <br>
                {{name}}
                <br>
                <b>Location</b>
                <br>
                {{location}}
            </div>
        </div>
    </div>
    <div class="form">
        <label for="name">What is your name ?</label>
        <br>
        <input v-model="name" type="text">
        <br>
        <label for="name">Where are you from ?</label>
        <br>
        <input v-model="location" type="text">
    </div>

</div>
</template>

<script>
export default {
    data() {
        return {
            name: '',
            location: ''
        }
    }

}
</script>

<style>
*,
*:before,
*:after {
    box-sizing: border-box;
}

body {
    font-family: monospace;
    background: seashell;
}

.content {
    margin: 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.card {
    background: skyblue;
    max-width: 600px;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 50px;
    border-radius: 10px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    transition: 500ms;
}

.card:hover {
    transform: scale(1.1);
}

.avatar {
    width: 70%;
}

.card-content {
    width: 200px;
    line-height: 30px;
    margin-right: 50px;
    text-align: justify;
    word-wrap: break-word;
}

.form {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    line-height: 30px;
    margin-top: 50px;
    font-weight: bold;
}

.form>input {
    width: 200%;
    padding: 5px;
    border-radius: 5px;
}
</style>
