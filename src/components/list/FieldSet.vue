<template>
  <fieldset>
    <legend>{{ legend }}</legend>
    <item v-for="(item, index) in items" :key="`item-${index}`" :item="item" @change="calculate" />
  </fieldset>
</template>

<script>
import Item from '@/components/list/Item.vue'

export default {
  name: 'FieldSet',
  components: { Item },
  props: {
    legend: {
      type: String,
      default: 'Legend'
    },
    items: {
      type: Array,
      default: () => []
    }
  },
  methods: {
    calculate(value) {
      this.$emit('change', value)
    }
  }
}
</script>
