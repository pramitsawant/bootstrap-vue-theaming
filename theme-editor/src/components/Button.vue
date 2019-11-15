<template>
  <div>
    <div class="mt-3">
      <b-button>Button</b-button>
      <b-button variant="danger">Button</b-button>
      <b-button variant="success">Button</b-button>
      <b-button variant="outline-primary">Button</b-button>
    </div>

    <div class="mt-3">
      <b-button>I am a Button</b-button>
      <b-button href="#">I am a Link</b-button>
    </div>

    <b-row>
      <b-col lg="4" class="pb-2"><b-button size="sm">Small Button</b-button></b-col>
      <b-col lg="4" class="pb-2"><b-button>Default Button</b-button></b-col>
      <b-col lg="4" class="pb-2"><b-button size="lg">Large Button</b-button></b-col>
    </b-row>

    <div class="mt-3">
      <b-button variant="primary">Primary</b-button>
      <b-button variant="secondary">Secondary</b-button>
      <b-button variant="success">Success</b-button>
      <b-button variant="danger">Danger</b-button>
      <b-button variant="warning">Warning</b-button>
      <b-button variant="info">Info</b-button>
      <b-button variant="light">Light</b-button>
      <b-button variant="dark">Dark</b-button>
    </div>    

    <div class="mt-3">
      <b-button variant="outline-primary">Primary</b-button>
      <b-button variant="outline-secondary">Secondary</b-button>
      <b-button variant="outline-success">Success</b-button>
      <b-button variant="outline-danger">Danger</b-button>
      <b-button variant="outline-warning">Warning</b-button>
      <b-button variant="outline-info">Info</b-button>
      <b-button variant="outline-light">Light</b-button>
      <b-button variant="outline-dark">Dark</b-button>
    </div>    

    <div class="mt-3">
      <b-button variant="link">Link</b-button>
    </div>

    <div class="mt-3">
      <b-button block variant="primary">Block Level Button</b-button>
    </div>    

    <div class="mt-3">
      <b-button pill>Button</b-button>
      <b-button pill variant="primary">Button</b-button>
      <b-button pill variant="outline-secondary">Button</b-button>
      <b-button pill variant="success">Button</b-button>
      <b-button pill variant="outline-danger">Button</b-button>
      <b-button pill variant="info">Button</b-button>
    </div>

    <div class="mt-3">
      <b-button squared>Button</b-button>
      <b-button squared variant="primary">Button</b-button>
      <b-button squared variant="outline-secondary">Button</b-button>
      <b-button squared variant="success">Button</b-button>
      <b-button squared variant="outline-danger">Button</b-button>
      <b-button squared variant="info">Button</b-button>
    </div>    

    <div class="mt-3">
      <b-button disabled size="lg" variant="primary">Disabled</b-button>
      <b-button disabled size="lg">Also Disabled</b-button>
    </div>

    <div class="mt-3">
      <h5>Pressed and un-pressed state</h5>
      <b-button :pressed="true" variant="success">Always Pressed</b-button>
      <b-button :pressed="false" variant="success">Not Pressed</b-button>

      <h5 class="mt-3">Toggleable Button</h5>
      <b-button :pressed.sync="myToggle" variant="primary">Toggle Me</b-button>
      <p>Pressed State: <strong>{{ myToggle }}</strong></p>

      <h5>In a button group</h5>
      <b-button-group size="sm">
        <b-button
          v-for="(btn, idx) in buttons"
          :key="idx"
          :pressed.sync="btn.state"
          variant="primary"
        >
          {{ btn.caption }}
        </b-button>
      </b-button-group>
      <p>Pressed States: <strong>{{ btnStates }}</strong></p>
    </div>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        myToggle: false,
        buttons: [
          { caption: 'Toggle 1', state: true },
          { caption: 'Toggle 2', state: false },
          { caption: 'Toggle 3', state: true },
          { caption: 'Toggle 4', state: false }
        ]
      }
    },
    computed: {
      btnStates() {
        return this.buttons.map(btn => btn.state)
      }
    }
  }
</script>


<style scoped lang="scss">

</style>
