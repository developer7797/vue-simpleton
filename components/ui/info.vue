<template>
  <div
    v-if="open"
    class="voice-settings-panel dark:!bg-[#404040] rounded-3xl border bg-white/80 backdrop-blur-2xl dark:text-white dark:border-[#525252] text-black !z-[1100000]"
    role="dialog"
    aria-label="About Fylepad"
  >
    <div
      class="fixed bg-red-600 rounded-full opacity-90 text-white right-0 -top-1 cursor-pointer"
      :onclick="close"
    >
      <svg xmlns="http://www.w3.org/2000/svg" width="24" viewBox="0 0 24 24">
        <path
          fill="currentColor"
          d="m12 13.4l-2.9 2.9q-.275.275-.7.275t-.7-.275t-.275-.7t.275-.7l2.9-2.9l-2.9-2.875q-.275-.275-.275-.7t.275-.7t.7-.275t.7.275l2.9 2.9l2.875-2.9q.275-.275.7-.275t.7.275q.3.3.3.713t-.3.687L13.375 12l2.9 2.9q.275.275.275.7t-.275.7q-.3.3-.712.3t-.688-.3z"
        />
      </svg>
    </div>

    <div class="flex items-center justify-between">
      <span class="text-xl drop-shadow-sm">fylepad</span>

      <span
        class="text-xl drop-shadow-sm tracking-tight"
        style="font-family: 'SpaceGrotesk'"
        >v2.2</span
      >
    </div>

    <p class="text-lg mt-3">Your perfect note-taking app!</p>
  </div>
</template>

<script lang="ts" setup>
const props = defineProps({
  open: {
    type: Boolean,
    required: true,
  },
  close: {
    type: Function,
    required: true,
  },
});
</script>

<style></style>
