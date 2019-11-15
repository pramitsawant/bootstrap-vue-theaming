<template>
  <div>

<b-container class="bv-example-row">

  <b-row>
    <b-col cols="6">

      <h3>Popover</h3>
      <div class="text-center my-3">
        <b-button v-b-popover.hover.top="'I am popover directive content!'" title="Popover Title">
          Hover Me
        </b-button>

        <b-button id="popover-target-1">
          Hover Me
        </b-button>
        <b-popover target="popover-target-1" triggers="hover" placement="top">
          <template v-slot:title>Popover Title</template>
          I am popover <b>component</b> content!
        </b-popover>
      </div>

      <b-container fluid>
        <h5 class="my-3">Placement</h5>
        <b-row>
          <b-col v-for="placement in placements" :key="placement" md="4" class="py-4 text-center" >
            <b-button :id="`popover-1-${placement}`" variant="primary">{{ placement }}</b-button>
            <b-popover :target="`popover-1-${placement}`" :placement="placement" title="Popover!" triggers="hover focus" :content="`Placement ${placement}`" ></b-popover>
          </b-col>
        </b-row>

        <h5 class="my-3">Content via properties or slots</h5>
        <b-row>
          <b-col md="6" class="py-4 text-center">
            <b-button id="popover-2" variant="primary">Using properties</b-button>
            <b-popover
              target="popover-2"
              title="Prop Examples"
              triggers="hover focus"
              content="Embedding content using properties is easy"
            ></b-popover>
          </b-col>

          <b-col md="6" class="py-4 text-center">
            <b-button id="popover-3" variant="primary">Using slots</b-button>
            <b-popover target="popover-3" triggers="hover focus">
              <template v-slot:title>Content via Slots</template>
              Embedding content <span class="text-danger">using slots</span> affords you
              <em>greater <strong>control.</strong></em> and basic HTML support.
            </b-popover>
          </b-col>
        </b-row>
      </b-container>

    </b-col>
    <b-col cols="6">
    <h3>Progress Bar</h3>
    <div>
      <b-progress :value="value" :max="max" show-progress animated></b-progress>
      <b-progress class="mt-2" :max="max" show-value>
        <b-progress-bar :value="value * (6 / 10)" variant="success"></b-progress-bar>
        <b-progress-bar :value="value * (2.5 / 10)" variant="warning"></b-progress-bar>
        <b-progress-bar :value="value * (1.5 / 10)" variant="danger"></b-progress-bar>
      </b-progress>

      <b-button class="mt-3" @click="randomValue">Click me</b-button>
    </div>

    <div>
      <h5>No label</h5>
      <b-progress :value="value" :max="max" class="mb-3"></b-progress>

      <h5>Value label</h5>
      <b-progress :value="value" :max="max" show-value class="mb-3"></b-progress>

      <h5>Progress label</h5>
      <b-progress :value="value" :max="max" show-progress class="mb-3"></b-progress>

      <h5>Value label with precision</h5>
      <b-progress :value="value" :max="max" :precision="2" show-value class="mb-3"></b-progress>

      <h5>Progress label with precision</h5>
      <b-progress :value="value" :max="max" :precision="2" show-progress class="mb-3"></b-progress>
    </div>

    <div>
      <h5>Custom label via default slot</h5>
      <b-progress :max="max" height="2rem">
        <b-progress-bar :value="value">
          Progress: <strong>{{ value.toFixed(2) }} / {{ max }}</strong>
        </b-progress-bar>
      </b-progress>

      <h5 class="mt-3">Custom label via property</h5>
      <b-progress :max="max">
        <b-progress-bar :value="value" :label="`${((value / max) * 100).toFixed(2)}%`"></b-progress-bar>
      </b-progress>

      <h5 class="mt-3">Custom label via property (HTML support)</h5>
      <b-progress :max="max">
        <b-progress-bar :value="value" :label-html="`<del>${value}</del>`"></b-progress-bar>
      </b-progress>
    </div>
    </b-col>
  </b-row>

</b-container>

<b-container class="bv-example-row">
  <b-row>
    <b-col cols="6">
    <h3>Spinner</h3>
    <div class="text-center">
      <b-spinner label="Spinning"></b-spinner>
      <b-spinner type="grow" label="Spinning"></b-spinner>
      <b-spinner variant="primary" label="Spinning"></b-spinner>
      <b-spinner variant="primary" type="grow" label="Spinning"></b-spinner>
      <b-spinner variant="success" label="Spinning"></b-spinner>
      <b-spinner variant="success" type="grow" label="Spinning"></b-spinner>
    </div>
    <b-button variant="primary" disabled>
      <b-spinner small></b-spinner>
      <span class="sr-only">Loading...</span>
    </b-button>

    <b-button variant="primary" disabled>
      <b-spinner small type="grow"></b-spinner>
      Loading...
    </b-button>

    </b-col>
    <b-col cols="6">
    <h3>Tooltip</h3>

<div class="text-center my-3">
  <b-button v-b-tooltip.hover title="Tooltip directive content">
    Hover Me
  </b-button>

  <b-button id="tooltip-target-1">
    Hover Me
  </b-button>
  <b-tooltip target="tooltip-target-1" triggers="hover">
    I am tooltip <b>component</b> content!
  </b-tooltip>
</div>


    </b-col>
  </b-row>
</b-container>


  </div>
</template>

<script>
  export default {
    data() {
      return {
        placements: [
          'topright',
          'top',
          'topleft',
          'bottomright',
          'bottom',
          'bottomleft',
          'righttop',
          'right',
          'lefttop',
          'rightbottom',
          'left',
          'leftbottom'
        ],
        value: 45,
        max: 100
      }
    },
    methods: {
      randomValue() {
        this.value = Math.random() * this.max
      },
    }
  }
</script>


<style scoped lang="scss">

</style>
