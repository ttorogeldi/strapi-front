<template>
  <v-menu offset-y open-on-hover>
    <template v-slot:activator="{ on, attrs }">
      <v-btn color="white" style="height:65px" class="white--text" text v-bind="attrs" v-on="on">
        {{ name }}
        <v-icon>mdi-chevron-down</v-icon>
      </v-btn>
    </template>
    <v-list>
      <v-list-item
          v-for="item in items"
          :key="item.id"
          @click="$router.push(item.link)">
        <v-list-item-title>
          {{ item.title }}
        </v-list-item-title>
      </v-list-item>
    </v-list>
  </v-menu>
</template>

<script>
export default {
  name: "MenuBlock",
  props: {
    items: {
      type: Array,
    },
    name: {
      type: String,
    }
  }
}
</script>

<style scoped>

</style>
