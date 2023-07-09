<script>
import Modal from './components/Modal.vue'
export default {
  data() {
    return {
     title: "My first Vue project",
     header: "Modal Title",
     text: "Let's try this",
     header2: "Modal Title",
     text2: "Let's try this",
     showModal: false,
     
    };
  },  
  components: {
      Modal
  },
  methods: {
    toggleModal(){
      this.showModal = !this.showModal
    },
    toggleModalTwo(){
      this.showModal = !this.showModal
    }
  }
};
</script>


<template> 
 <h1 class="title">{{ title }}</h1>
 <div v-if="showModal">
  <Modal :header="header" :text="text" theme="sale" @close="toggleModal"/>
 </div>
 <div v-if="showModal">
  <Modal :header="header" :text="text" @close="toggleModalTwo"/>
 </div>
 <h2>Welcome.....</h2>
 <button @click="toggleModal" class="btn">Open Modal</button> 
 <button @click="toggleModalTwo" class="btn">Open Modal 2</button> 
 

</template>

<style scoped>
.title{
  
  text-align: center;
  padding-top: 0px;
  border-bottom: 1px solid #ddd;
  /* display: inline-block; */
  
}

h2{
  text-align: center;
}
 .btn {
  margin-left: 47.5%;
}
</style>
