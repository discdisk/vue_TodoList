<template>
  <div>
      <form action="">
          <input type="text" name="title" placeholder="Add Todo...">
          <input type="submit" value="Submit" class="btn">
      </form>
  </div>

</template>

<script>
export default {
    name:"AddTodo"
}
</script>

<style scoped>
form{
    display: flex;
}
input[type="text"]{
    flex:10;
    padding: 5px;
}
input[type="submit"]{
    flex:2;
}
.btn{
  background-color: aquamarine;
  border: none;
  color: rgb(2, 2, 2);
  /* padding: 5px,3px; */
  /* text-align: center;
  text-decoration: none; */
  /* display: inline-block; */
  font-size: 20px;
  /* margin: 4px 5px; */
  float: right;
  /* border-radius: 20%; */
}
</style>