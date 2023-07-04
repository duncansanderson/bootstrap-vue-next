# BColorMode

<ClientOnly>
  <Teleport to=".bd-toc">

[[toc]]

  </Teleport>
</ClientOnly>

<div class="lead mb-5">

'BColorMode' is similar to [useColorMode](../composables/useColorMode.md) but provides a more low level directive for placement on individual components

</div>

## Demo

<HighlightCard>
  <BCard v-b-color-mode="currentColor">
    <BButton @click="changeColor">
      Current color: {{ currentColor }}
    </BButton>
  </BCard>
  <template #html>

```vue
<template>
  <BCard v-b-color-mode="currentColor">
    <BButton @click="changeColor"> Current color: {{ currentColor }} </BButton>
  </BCard>
</template>

<script setup lang="ts">
import {vBColorMode} from 'bootstrap-vue-next'

const currentColor = ref<'light' | 'dark'>('dark')

const changeColor = () => {
  currentColor.value = currentColor.value === 'dark' ? 'light' : 'dark'
}
</script>
```

  </template>

</HighlightCard>

<script setup lang="ts">
import {ref} from 'vue'
import {vBColorMode, BButton, BCard} from 'bootstrap-vue-next'
import HighlightCard from '../../components/HighlightCard.vue'

const currentColor = ref<'light' | 'dark'>('dark')

const changeColor = () => {
  currentColor.value = currentColor.value === 'dark' ? 'light' : 'dark'
}
</script>