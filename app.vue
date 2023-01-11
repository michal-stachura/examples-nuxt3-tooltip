<template>
  <div>
    <h1>Tooltip examples</h1>
    <hr />
    <h2>As directives</h2>
    <button v-tooltip="'Example tooltip text'">Hover me for tooltip</button>
    <button v-tooltip.right="'Example tooltip text'">Tooltip on the right</button>
    <h2>As component</h2>
    <div class="tooltips-container">
      <div>
        <VTooltip
          :placement="'right'"
          :distance="10"
        >
          <a>Hover me</a>
          <template #popper>
            Help me fund my Open Source work!
          </template>
        </VTooltip>
      </div>
      <div class="mt-4">
        <VDropdown>
          <button>Click me</button>
          <template #popper="{ hide }">
            <a @click="hide()">Click anywhere to Close</a>
          </template>
        </VDropdown>
      </div>
    </div>
  </div>
</template>


<style scoped>
.tooltips-container {
  display: inline-block;
}
.mt-4 {
  margin-block-start: 1rem;
}
</style>