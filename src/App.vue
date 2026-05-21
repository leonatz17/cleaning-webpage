<script>
import Nav from './components/Nav.vue';
import Home from './components/Home.vue';
import Footer from './components/Footer.vue';
import About from './components/About.vue';
import Services from './components/Services.vue';
import Faq from './components/Faq.vue';
import Contact from './components/Contact.vue';

export default{
  components:{
    Nav,
    Home,
    Footer,
    About,
    Services,
    Faq,
    Contact
    
  },
  data(){
    return {
      currentpage: 'Home'
    }
  },
  methods: {
    gotoPages(page){
      this.currentpage = page;
    }
  }
}

</script>

<template>
  <Nav @changepage="gotoPages" />
  <Home v-if="currentpage === 'Home'" />
  <About v-if="currentpage === 'About'" />
  <Services v-if="currentpage === 'Services'" />
  <Contact v-if="currentpage === 'Contact'" />
  <Faq v-if="currentpage === 'Faq' "/>
  <Footer />
  
</template>
