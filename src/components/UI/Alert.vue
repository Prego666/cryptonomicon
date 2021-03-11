<template>
  <div
    class="w-full border pl-4 pr-8 py-3 relative"
    :class="classes"
    role="alert"
  >
    <strong v-if="title" class="font-bold">{{ title }}</strong>
    <span v-if="text" class="block sm:inline">{{ text }}</span>
  </div>
</template>

<script>
export default {
  props: ["type", "title", "text"],
  computed: {
    classes() {
      const color = this.type;
      return [`bg-${color}-100`, `border-${color}-300`, `text-${color}-800`];
    }
  }
};
</script>

<style scoped>
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: scale(0.6);
}
.fade-enter-active {
  transition: all 0.4s ease;
}
.fade-leave-active {
  transition: all 0.4s ease;
  position: absolute;
}
</style>
