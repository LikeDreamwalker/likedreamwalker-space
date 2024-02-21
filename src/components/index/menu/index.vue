<template>
  <v-container class="fill-height">
    <v-responsive class="align-center justify-center text-center fill-height">
      <v-img height="300" src="@/assets/logo.svg" />

      <div class="text-body-2 font-weight-light mb-n1">Welcome to</div>

      <h1 class="text-h2 font-weight-bold">Vuetify</h1>

      <div class="py-14" />

      <div class="d-flex align-content-center justify-center">
        <v-hover v-slot="{ isHovering, props }">
          <v-card width="100px" v-bind="props" :elevation="isHovering ? 24 : 0" rounded='pill'>
            <v-card-title>{{ menuList[0].renderTitle }}</v-card-title>
          </v-card>
        </v-hover>
      </div>
    </v-responsive>
  </v-container>
</template>

<script setup>
import { ref } from 'vue'
const menuList = ref([
  {
    name: 'apps',
    renderTitle: '应用',
    renderSubtitle: 'apps',
    icon: '',
    to: '/apps'
  }
])
</script>
