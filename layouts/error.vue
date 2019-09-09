<template>
  <v-layout 
    wrap
    fill-height
    align-center
    justify-center>
    <v-flex 
      xs12
      md9
      text-xs-center
      class="web-component">
      <v-img
        style="display: block; margin-left: auto; margin-right: auto;"
        src="/undraw_page_not_found.png"
        contain
        width="100%"
      ></v-img>
      <span class="headline">{{ $t("error") }} </span>
      <v-flex pt-4>
        <v-btn 
          fab
          nuxt
          to="/"
          outline
          class="display-1">
          <font-awesome-icon class="primary-color" :icon="['fas', 'redo-alt']"/>
        </v-btn>
      </v-flex>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  props: ['error'],
}
</script>