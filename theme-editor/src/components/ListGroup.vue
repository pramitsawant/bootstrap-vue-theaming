<template>
  <div>
    <b-list-group>
      <b-list-group-item>Cras justo odio</b-list-group-item>
      <b-list-group-item>Dapibus ac facilisis in</b-list-group-item>
      <b-list-group-item>Morbi leo risus</b-list-group-item>
      <b-list-group-item>Porta ac consectetur ac</b-list-group-item>
      <b-list-group-item>Vestibulum at eros</b-list-group-item>
    </b-list-group>

    <b-list-group>
  <b-list-group-item>Cras justo odio</b-list-group-item>
  <b-list-group-item active>Dapibus ac facilisis in</b-list-group-item>
  <b-list-group-item>Morbi leo risus</b-list-group-item>
  <b-list-group-item>Porta ac consectetur ac</b-list-group-item>
  <b-list-group-item>Vestibulum at eros</b-list-group-item>
</b-list-group>

<b-list-group>
  <b-list-group-item href="#some-link">Awesome link</b-list-group-item>
  <b-list-group-item href="#" active>Link with active state</b-list-group-item>
  <b-list-group-item href="#">Action links are easy</b-list-group-item>
  <b-list-group-item href="#foobar" disabled>Disabled link</b-list-group-item>
</b-list-group>

<b-list-group>
  <b-list-group-item button>Button item</b-list-group-item>
  <b-list-group-item button>I am a button</b-list-group-item>
  <b-list-group-item button disabled>Disabled button</b-list-group-item>
  <b-list-group-item button>This is a button too</b-list-group-item>
</b-list-group>

<b-list-group>
  <b-list-group-item>Default list group item</b-list-group-item>
  <b-list-group-item variant="primary">Primary list group item</b-list-group-item>
  <b-list-group-item variant="secondary">Secondary list group item</b-list-group-item>
  <b-list-group-item variant="success">Success list group item</b-list-group-item>
  <b-list-group-item variant="danger">Danger list group item</b-list-group-item>
  <b-list-group-item variant="warning">Warning list group item</b-list-group-item>
  <b-list-group-item variant="info">Info list group item</b-list-group-item>
  <b-list-group-item variant="light">Light list group item</b-list-group-item>
  <b-list-group-item variant="dark">Dark list group item</b-list-group-item>
</b-list-group>

<b-list-group>
  <b-list-group-item href="#">Default list group item</b-list-group-item>
  <b-list-group-item href="#" variant="primary">Primary list group item</b-list-group-item>
  <b-list-group-item href="#" variant="secondary">Secondary list group item</b-list-group-item>
  <b-list-group-item href="#" variant="success">Success list group item</b-list-group-item>
  <b-list-group-item href="#" variant="danger">Danger list group item</b-list-group-item>
  <b-list-group-item href="#" variant="warning">Warning list group item</b-list-group-item>
  <b-list-group-item href="#" variant="info">Info list group item</b-list-group-item>
  <b-list-group-item href="#" variant="light">Light list group item</b-list-group-item>
  <b-list-group-item href="#" variant="dark">Dark list group item</b-list-group-item>
</b-list-group>

<b-list-group>
  <b-list-group-item class="d-flex justify-content-between align-items-center">
    Cras justo odio
    <b-badge variant="primary" pill>14</b-badge>
  </b-list-group-item>

  <b-list-group-item class="d-flex justify-content-between align-items-center">
    Dapibus ac facilisis in
    <b-badge variant="primary" pill>2</b-badge>
  </b-list-group-item>

  <b-list-group-item class="d-flex justify-content-between align-items-center">
    Morbi leo risus
    <b-badge variant="primary" pill>1</b-badge>
  </b-list-group-item>
</b-list-group>

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
