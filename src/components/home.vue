<template>
<div class="home component">
    <h1>{{ msg }}</h1>
    <button v-on:click="getData('button 2 is clicked')">Click here </button> 
    <button v-on:dblclick="getData('button 1 is clicked')">Click here</button>
    <h2>Please select the tech stack</h2>
    <label for="java">Java: </label>
    <input type="checkbox" value="java" name="stack" v-model="tech" id="java">
    <br>
    <label for="php">Php: </label>
    <input type="checkbox" value="Php" name="stack" v-model="tech" id="php">
    <br>
    <label for="node">Node: </label>
    <input type="checkbox" value="Node" name="stack" v-model="tech" id="node">
    <br>
    <h3>Selected tech stack is: {{tech}}</h3>
    <hr>
    <h2>Please select your profession</h2>
    <label for="student">Student: </label>
    <input type="radio" value="Student" name="prof" v-model="prof" id="student">
    <br>
    <label for="developer">Developer: </label>
    <input type="radio" value="Developer" name="prof" v-model="prof" id="developer">
    <br>
    <h3>Selected profession is: {{prof}}</h3>
    <br>
    <hr>
    <h3 v-if="show"> SPIT </h3>
    <h3 v-else> WOHLIG</h3>
    <button v-on:click="show=!show">Toggle</button>

</div>
</template>

<script>
export default {
    name: 'home',
    data()
    {
        return{
            tech: [],
            prof: [],
            show:true,
        }
    },
    props: {
        msg: String
    },
    methods: {
        getData(data) {
            alert(data);
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
h1 {
    color: orange
}
</style>
