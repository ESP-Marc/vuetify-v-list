<template>

  <v-app>

    <v-main>

      <v-card max-width="800" class="mx-auto">

        <v-card-text>

          <h2>VIcon accepts type Icon</h2>

          <v-icon :icon="IconChevronDown" size="32"/>
          <v-icon :icon="IconChevronUp" size="32"/>

          <v-divider class="my-4"/>

          <h2>Expand/Collapse icon has type error</h2>
          <small>Vue: Type Icon is not assignable to type string</small>

          <v-list
            :items="items"
            :expand-icon="IconChevronDown"
            :collapse-icon="IconChevronUp"
          />

        </v-card-text>

      </v-card>

    </v-main>

  </v-app>

</template>

<script lang="ts" setup>

import {IconChevronDown, IconChevronUp} from '@tabler/icons-vue'
import {ref} from 'vue'

const items = ref([
  {title: 'Title 1', children: [{title: 'Sub-Item 1A'}]},
  {title: 'Title 2', children: [{title: 'Sub-Item 2A'}]}])

</script>
