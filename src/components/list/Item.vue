<template>
  <div>
    <div v-if="item.pre">{{ item.pre }}</div>
    <label :for="id">
      <input type="checkbox" :id="id" :value="item.value" @click="switchCheck({id}, $event)"/>
      {{ item.text }}
    </label>
  </div>
</template>

<script>
export default {
  name: 'Item',
  props: {
    item: {
      type: Object,
      default: () => {}
    }
  },
  data() {
    return {
      id: null
    }
  },
  created () {
    this.id = this._uid
  },
  methods: {
    switchCheck (value, event) {
      if (event.target.checked) {
        this.$emit('change', this.item.value)
      }
      else {
        this.$emit('change', -(this.item.value))
      }
    }
  }
}
</script>
