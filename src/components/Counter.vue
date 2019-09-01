<template>
  <div class="counter">
    <h1>{{ msg }}</h1>
    <p>这是一个counter</p>
    <button v-on:click="clickPlus">{{click1}}</button>
    <button v-on:click="clickMun">{{click2}}</button>
    <br/>
    <p>{{ number }}</p>
  </div>
</template>

<script>
export default {
  name: 'Counter',
  props: {
    msg: String
  },
  data(){
    return {
                number: 0,
                click1: "点我+1",
                click2: "点我-1"
    }
        },
        methods:{
            clickPlus: function (){
                this.number ++;
            },
            clickMun: function (){
                this.number --;
            }
        }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
