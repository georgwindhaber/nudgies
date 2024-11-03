<script setup lang="ts">
import { meet } from '@googleworkspace/meet-addons/meet.addons'
const CLOUD_PROJECT_NUMBER = '1028257658812'

import { onMounted } from 'vue'

onMounted(async () => {
  const session = await meet.addon.createAddonSession({
    cloudProjectNumber: CLOUD_PROJECT_NUMBER,
  })
  const sidePanelClient = await session.createSidePanelClient()

  console.log(sidePanelClient)
})
</script>

<template>
  <main>Nudgies</main>
</template>
