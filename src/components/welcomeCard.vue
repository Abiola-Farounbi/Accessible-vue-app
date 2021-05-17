<template>
    <section>
        <h1> Welcome Message </h1>
        <hr>
        <p>
            Welcome to my Vue demo application
        </p>
        <label for="select-category"> Select Category </label><br>
        <select name="categories" id="select-category">
            <option v-for="category in categories" :key="category" > {{category}} </option>
        </select>
      
    </section>
</template>

<script>
export default {
  name: 'WelcomeCard',
  data() {
         return {
               categories:['Front-end','Back-end','UI/UX', 'Mobile']
            }
        },

}

 

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    main{
      margin:20px 10px;
    }
    h1{
      text-align: center;
    }
    section{
      width:70%;
      margin:10px auto;
      border:1px solid #472383;
      padding:10px ;
    }
    select{
      width:80%;
      padding: 10px 20px;
      margin:10px auto;
    }
 
    
</style>
