<template>
  <div>
    <label v-if="label">{{ label }}</label>
    <select
      :value="value"
      @input="updateValue"
      v-bind="$attrs"
      v-on="listeners"
    >
      <option
        v-for="option in options"
        :value="option"
        :key="option"
        :selected="option === value"
        >{{ option }}</option
      >
    </select>
  </div>
</template>

<script>
import { FormFieldMixin } from '../mixins/FormFieldMixin.js'

export default {
  mixins: [FormFieldMixin],
  props: {
    options: {
      type: Array,
      required: true
    }
  },
  computed: {
    listeners() {
      return {
        ...this.$listeners,
        input: this.updateValue
      }
    }
  }
}
</script>

<style></style>
