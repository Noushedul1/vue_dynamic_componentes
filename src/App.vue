<template>
  <button @click="toRender = 'compHome'">Home</button>
  <button @click="toRender = 'compContact'">Contact</button>
  <button @click="toRender = 'compAbout'">About</button>
  <keep-alive>
    <component :is="toRender"></component>
  </keep-alive>
</template>
<script>
  import compHome from './components/Home.vue';
  import compAbout from './components/About.vue';
  import compContact from './components/Contact.vue';
  export default{
    components: {
      compHome,
      compAbout,
      compContact
      },
    data(){
      return{
        toRender: 'compHome'
      }
    },
    methods: {
    },
    activate(){
      console.log('activated');
    },
    deactivated(){
      console.log('deactivated');
    }
  }
</script>
<style scoped>

</style>
