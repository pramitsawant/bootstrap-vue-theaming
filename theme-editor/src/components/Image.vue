<template>
  <div>
   <div>
  <b-img src="https://picsum.photos/1024/400/?image=41" fluid alt="Responsive image"></b-img>
</div>

<div>
  <h5>Small image with <code>fluid</code>:</h5>
  <b-img src="https://picsum.photos/300/150/?image=41" fluid alt="Fluid image"></b-img>

  <h5 class="my-3">Small image with <code>fluid-grow</code>:</h5>
  <b-img src="https://picsum.photos/300/150/?image=41" fluid-grow alt="Fluid-grow image"></b-img>
</div>


<b-container fluid class="p-4 bg-dark">
  <b-row>
    <b-col>
      <b-img thumbnail fluid src="https://picsum.photos/250/250/?image=54" alt="Image 1"></b-img>
    </b-col>
    <b-col>
      <b-img thumbnail fluid src="https://picsum.photos/250/250/?image=58" alt="Image 2"></b-img>
    </b-col>
    <b-col>
      <b-img thumbnail fluid src="https://picsum.photos/250/250/?image=59" alt="Image 3"></b-img>
    </b-col>
  </b-row>
</b-container>

<template>
  <div>
    <b-img v-bind="mainProps" rounded alt="Rounded image"></b-img>
    <b-img v-bind="mainProps" rounded="top" alt="Top-rounded image"></b-img>
    <b-img v-bind="mainProps" rounded="right" alt="Right-rounded image"></b-img>
    <b-img v-bind="mainProps" rounded="bottom" alt="Bottom-rounded image"></b-img>
    <b-img v-bind="mainProps" rounded="left" alt="Left-rounded image"></b-img>
    <b-img v-bind="mainProps" rounded="circle" alt="Circle image"></b-img>
    <b-img v-bind="mainProps" rounded="0" alt="Not rounded image"></b-img>
  </div>
</template>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        mainProps: { blank: true, blankColor: '#777', width: 75, height: 75, class: 'm1' }
      }
    }
  }
</script>


<style scoped lang="scss">

</style>
