<template>
  <div id="app">
    <Header />
    <AddTodo/>
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo"/>
    <p id=welcom>
      welcome to my first vue project {{msg}}!!
    </p>
    
  </div>
  
</template>

<script>
import Todos from './components/Todos'
import AddTodo from './components/AddTodo'
import Header from './components/Header'
export default {
  name: 'app',
  components: {
    Header,
    Todos,
    AddTodo
  },
  data(){
    return{
      msg:'discdisk',
      todos:[
        {
          id:1,
          title:'one',
          complete:false
        },
        {
          id:2,
          title:'two',
          complete:false
        },
        {
          id:3,
          title:'three',
          complete:false
        }
      ]
    }
  },
  methods:{
    deleteTodo(id){
      console.log(id)
      this.todos = this.todos.filter(todo => todo.id !== id);
    }
  }
}
</script>

<style>
#welcom{
  font-size:xx-large;
  color:aquamarine;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>
