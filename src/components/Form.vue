<template>
      <section>
          <h1> Contact Form </h1>
           <form  autocomplete="on">
             <label for="name">Name</label> <br>
             <input type="text" name="name" id="name" v-model="name"  /><br>
             <label for="email"> Email </label><br>
             <input type="email" name="email" id="email" v-model="email"  /><br>
             <label for="message"> Message </label><br>
             <textarea id='message' v-model="message" ></textarea><br>
            <button type="submit" 
            @keydown.enter ="submitted = true"
            @click.prevent="submitted = true"  
            >
              Submit
            </button>
          </form>

       </section>
       <section class='displayOutput' v-if="submitted">
          <h2> Display Output </h2>
          <ul>
            <li> {{name}} </li>
            <li> {{email}} </li>
            <li> {{message}}</li>
          </ul>
       </section>
</template>

<script>
export default {
  name: 'Form',
  data() {
         return {
                name: '',
                email: '',
                message: '',
                submitted: false,
        
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
    input, textarea{
      width:80%;
      padding: 10px 20px;
      margin:10px auto;
    }
    button{
      padding: 10px 20px;
      border:none;
      background-color: #472383;
      color:white;
    }
    li{
      list-style-type: none;
    }
    
</style>
