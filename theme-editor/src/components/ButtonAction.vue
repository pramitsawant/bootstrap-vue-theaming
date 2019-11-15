<template>
  <div>

   <div class="my-2">

    <b-tabs card>
        
            <b-tab title="Button" active><Button/></b-tab>
            <b-tab title="Button Group"><ButtonGroup/></b-tab>
            <b-tab title="Button Toolbar"><ButtonToolbar/></b-tab>    
    </b-tabs>

    </div>

  </div>
</template>

<script>


import Button from '@/components/Button.vue'
import ButtonGroup from '@/components/ButtonGroup.vue'
import ButtonToolbar from '@/components/ButtonToolbar.vue'



export default {
  components: {
  Button,
  ButtonGroup,
  ButtonToolbar
  },

    data() {
      return {
        form: {
          email: '',
          name: '',
          food: null,
          checked: []
        },
        foods: [{ text: 'Select One', value: null }, 'Carrots', 'Beans', 'Tomatoes', 'Corn'],
        show: true
      }
    },
    methods: {
      onSubmit(evt) {
        evt.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(evt) {
        evt.preventDefault()
        // Reset our form values
        this.form.email = ''
        this.form.name = ''
        this.form.food = null
        this.form.checked = []
        // Trick to reset/clear native browser form validation state
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    }
  }
</script>


<style scoped lang="scss">

</style>
