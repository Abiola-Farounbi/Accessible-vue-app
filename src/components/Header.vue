<template>
    <header>
      <img src='../assets/logo.png' alt='Vue logo'/>
      <h1> Header </h1>
    </header>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header{
  background-color: #472383;
  padding:10px;
  text-align: center;
  color:white;
}
img
{
    width:50px;
    height:50px;
    display:flex;
    margin:0px auto;
}
</style>
