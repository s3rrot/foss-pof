<template>
  <div>
    <div v-for="(fieldset, index) in fieldsets" :key="`fieldset-${index}`">
      <field-set :legend="fieldset.legend" :items="fieldset.items" @change="calculate" />
      {{ fieldset.value }}
    </div>

    === FAIL METER ===
    <ul>
      <li>0 points of FAIL: Perfect! All signs point to success!</li>
      <li>5-25 points of FAIL: You're probably doing okay, but you could be better.</li>
      <li>30-60 points of FAIL: Babies cry when your code is downloaded</li>
      <li>65-90 points of FAIL: Kittens die when your code is downloaded</li>
      <li>95-130 points of FAIL: HONK HONK. THE FAILBOAT HAS ARRIVED!</li>
      <li>135+ points of FAIL: So much fail, your code should have its own reality TV show.</li>
    </ul>

    <div>
      FAIL METER: {{ totalCalculation }}
    </div>
  </div>
</template>

<script>
import FieldSet from '@/components/list/FieldSet.vue'

import size from '@/components/list/json/size.json'
import sourceControl from '@/components/list/json/source_control.json'
import bundleFromSource from '@/components/list/json/bundle_from_source.json'
import bundling from '@/components/list/json/bundling.json'
import libraries from '@/components/list/json/libraries.json'
import systemInstall from '@/components/list/json/system_install.json'
import codeOdditiesInstall from '@/components/list/json/code_oddities.json'
import communication from '@/components/list/json/communication.json'
import releases from '@/components/list/json/releases.json'
import history from '@/components/list/json/history.json'
import licensing from '@/components/list/json/licensing.json'
import documentation from '@/components/list/json/documentation.json'

export default {
  components: { FieldSet },
  name: 'List',
  data() {
    return {
      totalCalculation: 0,
      fieldsets: [
        ...size.fieldsets,
        ...sourceControl.fieldsets,
        ...bundleFromSource.fieldsets,
        ...bundling.fieldsets,
        ...libraries.fieldsets,
        ...systemInstall.fieldsets,
        ...codeOdditiesInstall.fieldsets,
        ...communication.fieldsets,
        ...releases.fieldsets,
        ...history.fieldsets,
        ...licensing.fieldsets,
        ...documentation.fieldsets
      ]
    }
  },
  methods: {
    calculate(value) {
      this.totalCalculation += value
    }
  }
}
</script>
