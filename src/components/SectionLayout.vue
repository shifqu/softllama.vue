<template>
  <section class="section-layout">
    <v-container class="py-0">
      <h2
        :id="title.toLowerCase()"
        class="headline text-xs-center py-5 font-weight-bold text-uppercase blue-grey--text text--darken-3"
      >
        {{ title }}
      </h2>
      <v-divider />
      <div class="py-5">
        <slot></slot>
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  props: ['title']
}
</script>
