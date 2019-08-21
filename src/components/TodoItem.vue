<template>
    <div class=card v-bind:class="{'is-copmplete':todo.complete}">

    <p>
      <input type="checkbox" v-on:change="markComplete" value="1">
      {{todo.title}}
      <button class='button' @click="$emit('del-todo',todo.id)" >x</button>
    </p>

    </div>
</template>

<script>
export default {
    name:"TodoItem",
    props:["todo"],
    methods:{
      markComplete(){
        this.todo.complete =! this.todo.complete;
      }
    }
}
</script>

<style scoped>
.is-copmplete{
  text-decoration-line: line-through;
}

.button {
  background-color: #4CAF50;
  border: none;
  color: white;
  /* padding: 5px,3px; */
  text-align: center;
  text-decoration: none;
  /* display: inline-block; */
  font-size: 10px;
  margin: 4px 5px;
  float: right;
  border-radius: 20%;
}


.card{
  /* display: block; */
  background-color:rgb(243, 240, 240);
  color:orangered;
  text-align: left;
  padding: 1px;
  border-bottom:1px #4CAF50 solid ;

  border-radius: 2px;
  /* width: 100px; */
  /* vertical-align: middle; */
  }
.card:hover{
  color:chartreuse;
}
</style>