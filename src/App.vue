<template>
  <Header></Header>
  <main>
 <section class='pageOptions'>
   <button @click="selectedComponent = 'WelcomeCard'" > Welcome Message </button> 
  <button @click="selectedComponent = 'Form'" > Contact Form </button> 
  
 </section>
  
  <!-- binding the current component to the property  -->
  <component :is="selectedComponent"></component>
  </main>
  <Footer></Footer>
</template>

<script>
import Header from './components/Header.vue'
import WelcomeCard from './components/welcomeCard.vue'
import Form from './components/Form.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    WelcomeCard,
    Form,
    Footer
  },
   data:function(){
    return{
     selectedComponent: "WelcomeCard"
    }
  }
}
</script>

<style>
*{
  margin:0px;
  padding:0px;
}
.pageOptions {
  margin:0px 0px 20px 0px;
}
.pageOptions button{
  border:1px solid #472383;
  padding:10px;
  font-size: 18px;
}
.pageOptions button:hover{
  background: #472383;
  color:white;
}
</style>
