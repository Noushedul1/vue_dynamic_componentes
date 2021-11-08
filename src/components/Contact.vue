<template>
  <p>Contact page</p>
  <form v-on:submit.prevent="formvalue">
      <div>
          <label>First name : </label>
          <input type="text" v-model="formdata.firstname">
      </div>
      <div>
          <label>Last name : </label>
          <input type="text" v-model="formdata.lastname">
      </div>
      <div>
          <label>Password : </label>
          <input type="password" v-model="formdata.pass">
      </div>
      <div>
          <input type="submit" value="submit">
      </div>
      <div v-if="isSubmitted">
          <h1>Form data</h1>
          <p>First name : {{formdata.firstname}}</p>
          <p>Last name : {{formdata.lastname}}</p>
          <p>Password : {{formdata.pass}}</p>
      </div>
  </form>
</template>
<script>
    export default{
        data(){
            return{
                formdata: {
                    firstname: '',
                    lastname: '',
                    pass: ''
                },
                isSubmitted: false
            }
        },
        methods: {
            formvalue: function(){
                this.isSubmitted = true;
            }
        }
    }
</script>
<style scoped>

</style>