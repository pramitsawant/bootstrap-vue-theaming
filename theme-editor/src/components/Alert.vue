<template>
  <div>
  <div>
    <b-alert show variant="primary">Primary Alert</b-alert>
    <b-alert show variant="secondary">Secondary Alert</b-alert>
    <b-alert show variant="success">Success Alert</b-alert>
    <b-alert show variant="danger">Danger Alert</b-alert>
    <b-alert show variant="warning">Warning Alert</b-alert>
    <b-alert show variant="info">Info Alert</b-alert>
    <b-alert show variant="light">Light Alert</b-alert>
    <b-alert show variant="dark">Dark Alert</b-alert>
  </div>


  <div>
  <b-alert show variant="success">
    <h4 class="alert-heading">Well done!</h4>
    <p>
      Aww yeah, you successfully read this important alert message. This example text is going to
      run a bit longer so that you can see how spacing within an alert works with this kind of
      content.
    </p>
    <hr>
    <p class="mb-0">
      Whenever you need to, be sure to use margin utilities to keep things nice and tidy.
    </p>
  </b-alert>
</div>

<div>
  <b-alert show variant="primary"><a href="#" class="alert-link">Primary Alert</a></b-alert>
  <b-alert show variant="secondary"><a href="#" class="alert-link">Secondary Alert</a></b-alert>
  <b-alert show variant="success"><a href="#" class="alert-link">Success Alert</a></b-alert>
  <b-alert show variant="danger"><a href="#" class="alert-link">Danger Alert</a></b-alert>
  <b-alert show variant="warning"><a href="#" class="alert-link">Warning Alert</a></b-alert>
  <b-alert show variant="info"><a href="#" class="alert-link">Info Alert</a></b-alert>
  <b-alert show variant="light"><a href="#" class="alert-link">Light Alert</a></b-alert>
  <b-alert show variant="dark"><a href="#" class="alert-link">Dark Alert</a></b-alert>
</div>

<div>
  <b-alert show dismissible>
    Dismissible Alert! Click the close button over there <b>&rArr;</b>
  </b-alert>
</div>


  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>


<style scoped lang="scss">

</style>
