<template>
  <div>
    <b-breadcrumb :items="items"></b-breadcrumb>

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
