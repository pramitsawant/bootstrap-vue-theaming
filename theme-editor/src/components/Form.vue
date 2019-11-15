<template>
  <div>

   <div class="my-2">

    <b-tabs card>
        <b-tab title="Form Check Box" active><FormCheckBox/></b-tab>
        <b-tab title="Form File"><FormFile/></b-tab>
        <b-tab title="Form Group"><FormGroup/></b-tab>
        <b-tab title="Form Input"><FormInput/></b-tab>
        <b-tab title="Form Radio"><FormRadio/></b-tab>
        <b-tab title="Form Select"><FormSelect/></b-tab>     
        <b-tab title="Form Textarea"><FormTextarea/></b-tab>
        <b-tab title="Input Group"><Inputgroup/></b-tab>     
    </b-tabs>

    </div>

  </div>
</template>

<script>


import FormCheckBox from '@/components/FormCheckBox.vue'
import FormFile from '@/components/FormFile.vue'
import FormGroup from '@/components/FormGroup.vue'

import FormInput from '@/components/FormInput.vue'
import FormRadio from '@/components/FormRadio.vue'
import FormSelect from '@/components/FormSelect.vue'
import FormTextarea from '@/components/FormTextarea.vue'
import Inputgroup from '@/components/Inputgroup.vue'



export default {
  components: {
  FormCheckBox,
  FormFile,
  FormGroup,
  FormInput,
  FormRadio,
  FormSelect,
  FormTextarea,
  Inputgroup
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
