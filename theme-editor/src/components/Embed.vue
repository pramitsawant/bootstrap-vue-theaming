<template>
  <div>
    <div class="m-5">
  <b-embed
    type="iframe"
    aspect="16by9"
    src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0"
    allowfullscreen
  ></b-embed>
</div>

<div class="m-5">
  <b-embed type="video" aspect="4by3" controls poster="poster.png">
    <source src="dev-stories.webm" type="video/webm">
    <source src="dev-stories.mp4" type="video/mp4">
  </b-embed>
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
