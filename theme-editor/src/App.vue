<template>
  <div id="app" > 
  <b-container fluid class="bv-example-row bg-dark">  
   <div class="d-flex flex-row-reverse">
     <div class="p-2"><b-form-checkbox @change="changeTheme" v-model="checked" size="lg" name="check-button" switch value="dark" unchecked-value="light" >Theme <b>({{ checked }})</b></b-form-checkbox></div>
   </div>  
    <router-view/>
    </b-container>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        checked: "light",
        datatheme: null,
      }
    },
    mounted: function() {
      this.datatheme = this.$el.getAttribute('data-theme');
    },
    methods: {
    changeTheme(val){
    console.log(val)
    console.log(this.datatheme)

    }

    
    }
  }
</script>
<style lang="scss">

</style>
