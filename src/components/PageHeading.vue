<template>
  <div class="md:flex md:items-center md:justify-between">
    <div class="flex-1 min-w-0">
      <h2 class="text-2xl font-bold leading-7 text-gray-900 sm:text-3xl sm:truncate">
        {{ title }}
      </h2>
    </div>
    <div class="mt-4 flex md:mt-0 md:ml-4" v-if="showButton">
      <router-link :to="button.path" type="button" class="ml-3 inline-flex items-center px-4 py-2 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
        {{ button.label }}
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "PageHeading",
  props: ['title', 'button'],
  computed: {
    showButton() {
      return this.button !== undefined;
    }
  }
}
</script>

<style scoped>

</style>