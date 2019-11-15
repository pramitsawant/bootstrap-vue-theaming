<template>
  <div>
   <div>
  <b-form-group label="Small:" label-for="file-small" label-cols-sm="2" label-size="sm">
    <b-form-file id="file-small" size="sm"></b-form-file>
  </b-form-group>

  <b-form-group label="Default:" label-for="file-default" label-cols-sm="2">
    <b-form-file id="file-default"></b-form-file>
  </b-form-group>

  <b-form-group label="Large:" label-for="file-large" label-cols-sm="2" label-size="lg">
    <b-form-file id="file-large" size="lg"></b-form-file>
  </b-form-group>
</div>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        items: [
          {
            text: 'Admin',
            href: '#'
          },
          {
            text: 'Manage',
            href: '#'
          },
          {
            text: 'Library',
            active: true
          }
        ]
      }
    }
  }
</script>


<style scoped lang="scss">

</style>
