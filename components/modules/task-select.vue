<template>
  <div>
    <div class="task-input-wrapper">
      <select
        v-if="items"
        id=""
        ref="el"
        class="task-select-field"
        :class="{ error: error }"
        name=""
        :value="value"
        data-value=""
        @input="onChange"
        @change="onChange"
      >
        <option v-for="item in items" :key="item.value" :value="item.value">
          {{ item.text }}
        </option>
        <slot></slot>
      </select>
      <label class="task-input-label">{{ label }}</label>
      <span class="dropdown-icon">
        <svg
          width="10"
          height="5"
          viewBox="0 0 10 5"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M4.99995 5L0.669823 -2.18762e-06L9.33008 -1.43051e-06L4.99995 5Z"
            fill="white"
          />
        </svg>
      </span>
    </div>
    <span v-if="errorMessage" class="mt-5 text-xs tooltip px-4 py-3 w-full">
      {{ errorMessage }}
    </span>
  </div>
</template>

<script>
export default {
  name: 'TaskSelect',
  props: {
    value: {},
    label: { type: String, default: '' },
    items: { type: Array, default: () => [{ text: '', value: '' }] },
    error: { type: Boolean },
    errorMessage: { type: String, default: '' },
  },
  emits: ['input'],
  mounted() {
    if (this.value) {
      this.$refs.el.setAttribute('data-value', this.value)
    }
  },
  methods: {
    onChange(e) {
      this.$emit('input', e.target.value)
      e.target.setAttribute('data-value', e.target.value)
    },
  },
}
</script>

<style scoped src="~~/assets/css/main.css"></style>
<style scoped>
.dropdown-icon {
  position: absolute;
  right: 0;
  top: 0;
  bottom: 0;
  display: flex;
  align-items: center;
  padding-right: 1rem;
  pointer-events: none;
}

.dropdown-icon > svg {
  height: 20px;
  width: 20px;
  color: #a9abb0;
}
</style>
