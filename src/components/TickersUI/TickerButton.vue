<template>
  <button
    type="button"
    class="m-2 px-4 bg-gray-400 text-white p-2 rounded leading-none flex items-center"
  >
    {{ caption }}
  </button>
</template>

<script>
export default {
  props: ["caption"]
};
</script>

<style></style>
