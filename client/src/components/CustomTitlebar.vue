<template>
  <div class="custom-title-bar">
    <!-- Window drag area -->
    <div class="window-drag-area"></div>
    <!-- Custom buttons -->
    <div class="window-buttons">
      <!-- Minimize window button -->
      <button class="window-button" @click="minimizeWindow">
        <svg width="20" height="20" viewBox="0 0 24 24">
          <rect x="3" y="11" width="18" height="2" fill="currentColor" />
        </svg>
      </button>
      <!-- Maximize window button -->
      <button class="window-button" @click="maximizeWindow">
        <svg width="20" height="20" viewBox="0 0 24 24">
          <rect
            x="3"
            y="3"
            width="16"
            height="16"
            fill="none"
            stroke="currentColor"
            stroke-width="2.5"
          />
        </svg>
      </button>
      <!-- Close window button -->
      <button class="window-button close" @click="closeWindow">
        <svg width="20" height="20" viewBox="0 0 24 24">
          <path
            stroke="currentColor"
            stroke-linecap="round"
            stroke-width="2.5"
            d="M6 6l12 12m0-12L6 18"
          />
        </svg>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    minimizeWindow() {
      window.electronAPI.minimize();
    },

    maximizeWindow() {
      window.electronAPI.maximize();
    },

    closeWindow() {
      window.electronAPI.close();
    },
  },
};
</script>
