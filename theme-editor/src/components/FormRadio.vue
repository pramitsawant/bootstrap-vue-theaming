<template>
  <div>

     <div>
    <b-form-group label="Individual radios">
      <b-form-radio v-model="selected" name="some-radios" value="first">Option A</b-form-radio>
      <b-form-radio v-model="selected" name="some-radios" value="second">Option B</b-form-radio>
    </b-form-group>

    <div class="mt-3">Selected: <strong>{{ selected }}</strong></div>
  </div>

  <div>
    <b-form-group label="Inline radios (default)">
      <b-form-radio-group
        v-model="selected"
        :options="options"
        name="radio-inline"
      ></b-form-radio-group>
    </b-form-group>

    <b-form-group label="Stacked radios">
      <b-form-radio-group
        v-model="selected"
        :options="options"
        name="radios-stacked"
        stacked
      ></b-form-radio-group>
    </b-form-group>

    <div class="mt-3">Selected: <strong>{{ selected }}</strong></div>
  </div>


<div>
  <b-form-radio name="radio-size" size="sm">Small</b-form-radio>
  <b-form-radio name="radio-size">Default</b-form-radio>
  <b-form-radio name="radio-size" size="lg">Large</b-form-radio>
</div>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        selected: null,
         options: [
         { text: 'First radio', value: 'first' },
        { text: 'Second radio', value: 'second' },
        { text: 'Third radio', value: 'third' },
        ],
      }
    }
  }
</script>


<style scoped lang="scss">



</style>
