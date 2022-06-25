<template>
  <div class="relative">
    <div class="task-input-wrapper">
      <input
        :type="type"
        class="task-input-field"
        :class="{ error: error }"
        placeholder="_"
        :value="value"
        v-bind="$attrs"
        @input="onChange"
      />
      <label class="task-input-label">{{ label }}</label>
      <div v-if="prepend" class="prepend">{{ prepend }}</div>
    </div>
    <div class="absolute">
      <span v-if="errorMessage" class="mt-3 text-xs tooltip px-4 py-3 w-full">
        {{ errorMessage }}
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TaskInput',
  props: {
    label: { type: String, default: '' },
    error: { type: Boolean, default: false },
    errorMessage: { type: String, default: '' },
    value: {},
    prepend: { type: String, default: '' },
    type: { type: String, default: 'text' },
  },
  // emits: ['update:modelValue'],
  emits: ['input'],
  methods: {
    onChange(e) {
      this.$emit('input', e.target.value)
    },
  },
}
</script>

<style scoped src="~~/assets/css/main.css"></style>

<style scoped>
.prepend {
  position: absolute;
  left: 0;
  top: 0;
  padding: 12px 10px;
  font-size: 14px;
}
</style>
