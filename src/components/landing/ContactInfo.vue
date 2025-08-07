<template>
  <section class="contact-section">

    <v-container class="text-center py-8">
      <h1 class="text-h3 font-weight-bold gradient-text">Connect with Me</h1>
      <p class="text-h5  mt-2">
        I'm always open to new opportunities and collaborations. Feel free to reach out via email or connect with me on social media.
      </p>
    </v-container>
    <v-spacer />
    <!-- Social Links -->
    <div class="social-links">
      <a aria-label="Facebook" href="https://www.facebook.com/ekilvalencia" target="_blank">
        <span class="mdi mdi-facebook mdi-48px" />
      </a>
      <a aria-label="Instagram" href="https://www.instagram.com/zikvalencia" target="_blank">
        <span class="mdi mdi-instagram mdi-48px" />
      </a>
      <a aria-label="Threads" href="https://www.threads.com/@zikvalencia" target="_blank">
        <span class="mdi mdi-at mdi-48px" /> <!-- Threads placeholder -->
      </a>
      <a aria-label="LinkedIn" href="https://www.linkedin.com/in/exequiel-valencia-279333254/" target="_blank">
        <span class="mdi mdi-linkedin mdi-48px" />
      </a>
    </div>

    <!-- Email and Phone (crawler-safe) -->
    <div class="contact-info">
      <div class="info-row">
        📧 <span ref="emailEl" />
      </div>
      <div class="info-row">
        📞 <span ref="phoneEl" />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
  import { onMounted, ref } from 'vue'

  const emailEl = ref<HTMLElement | null>(null)
  const phoneEl = ref<HTMLElement | null>(null)

  onMounted(() => {
    // Obfuscate to protect from crawlers
    if (emailEl.value) {
      emailEl.value.textContent = 'valencia.exequiel123' + '@' + 'gmail.com'
    }
    if (phoneEl.value) {
      phoneEl.value.textContent = '+81 80-6192-1137'
    }
  })
</script>

<style scoped>
.contact-section {
  padding: 2rem 1rem;
  text-align: center;

  color: #f0f0f0;

  max-width: 700px;
  margin: 0 auto;

}

.section-title {
  font-size: 2rem;
  margin-bottom: 1.5rem;
  color: #00a28c;
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 1.5rem;
  margin-bottom: 2rem;
}

.social-links a {
  color: #ccc;
  transition: color 0.3s;
}

.social-links a:hover {
  color: #00a28c;
}

.contact-info {
  font-size: 1.1rem;
  line-height: 1.8;
  color: #e0e0e0;
}

.info-row {
  margin-top: 0.75rem;
}
</style>
