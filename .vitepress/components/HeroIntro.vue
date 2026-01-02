<script setup>
defineProps({
  logo: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="hero-intro">
    <img :src="logo" alt="FOSSASIA Logo" class="hero-logo" />

    <div class="hero-text">
      <div>Open Tech Summit</div>
      <div>Bangkok, Thailand</div>
      <div>March 8–10, 2026</div>
    </div>
  </div>
</template>

<style scoped>
.hero-intro {
  display: flex;
  align-items: stretch; /* ensures logo matches text height */
  gap: 16px;
  margin-bottom: 20px;
}

.hero-text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  font-size: 13px;
  font-weight: 400; /* normal */
  line-height: 1.4;
  color: var(--vp-c-text-1);
}

/* Logo scales to text column height */
.hero-logo {
  align-self: center;
  height: 100%;
  max-height: calc(11px * 3 * 1.4); /* 3 lines × line-height */
  object-fit: contain;
}
</style>
