<template>
   <v-container class="text-center my-8">
        <v-row
            class="mb-4"
            style="position: sticky; top: 0; z-index: 10; background: white;"
        >
            <v-col cols="12">
            <v-btn
                v-for="item in ['Home', 'About', 'Contact']"
                :key="item"
                class="mx-2 "
                size="x-large"
                :to="`/${item.toLowerCase()}`"
                variant="text"
            >
                {{ item }}
            </v-btn>
            </v-col>
        </v-row>
        <v-img
            class="mb-4"
            height="150"
            src="@/assets/logo.png"
        />
        <h1 class="text-h2 font-weight-bold">ZIK STUDIOS</h1>
        <div class="text-body-2 font-weight-light mb-n1">Welcome to my website</div>
    </v-container>

</template>

<script lang="ts" setup>
  //
</script>
