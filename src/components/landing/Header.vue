<template>
  <div class="header-wrapper">
    <v-container class="text-center">

      <!-- Mobile: hamburger left, logo right -->
      <div class="d-flex d-md-none align-center justify-space-between mobile-header">
        <v-btn aria-label="Open menu" icon @click="drawer = true">
          <v-icon icon="mdi-menu" />
        </v-btn>
        <v-img
          alt="Zik logo"
          class="mobile-logo"
          contain
          src="@/assets/zik-logo.svg"
        />
      </div>

      <!-- Desktop/Tablet: big logo and buttons -->
      <div class="d-none d-md-block">
        <v-img
          alt="Zik logo"
          class="mb-4 mx-auto"
          height="300"
          src="@/assets/zik-logo.svg"
        />
        <v-col class="d-flex justify-center flex-wrap" cols="12">
          <v-btn
            v-for="item in navItems"
            :key="item.id"
            class="mx-2 text-h4"
            :href="`#${item.id}`"
            size="x-large"
            variant="text"
            @click.prevent="scrollTo(item.id)"
          >
            {{ item.label }}
          </v-btn>
        </v-col>
      </div>

    </v-container>

    <!-- Mobile drawer -->
    <v-navigation-drawer
      v-model="drawer"
      aria-label="Mobile navigation"
      location="top"
      :scrim="true"
      temporary
    >
      <v-list density="comfortable" nav>
        <v-list-item
          v-for="item in navItems"
          :key="item.id"
          :title="item.label"
          @click="handleNav(item.id)"
        />
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script lang="ts" setup>
  import { ref } from 'vue'

  const drawer = ref(false)

  const navItems = ref([
    { label: 'Home', id: 'home' },
    { label: 'About', id: 'about' },
    { label: 'Skills', id: 'skills' },
    { label: 'Experience', id: 'experience' },
    { label: 'Contact', id: 'contact' },
  ])

  function scrollTo (id: string) {
    const el = document.querySelector(`#${id}`)
    if (el) (el as HTMLElement).scrollIntoView({ behavior: 'smooth', block: 'start' })
  }
  function handleNav (id: string) {
    drawer.value = false
    requestAnimationFrame(() => scrollTo(id))
  }
</script>

<style scoped>
.header-wrapper {
  padding-block: 20px;
}

/* Mobile-specific header bar */
.mobile-header {
  height: 60px;
  padding-inline: 8px;
}

.mobile-logo {
  height: 40px;
  width: auto;
}
</style>
