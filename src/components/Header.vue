<template>
  <header class = "header">
      <div class = "headLogo">
        <img  alt="Vue logo" src="../assets/logo.png"  width="70px">
        <h1>
          TodoList
        </h1> 
      </div>

  </header>

</template>

<script>
export default {
    name:"Header"
}
</script>

<style scoped>
.header{
    background: #333;
    color: aliceblue;
    /* text-emphasis: circle; */
    text-align: center;
    padding: 10px;
}
.headLogo{
    
    display: inline-flex;
    height:80px;
    align-items: center;
}

</style>