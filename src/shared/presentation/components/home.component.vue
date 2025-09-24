<script setup lang="js">
import { Toolbar as PvToolbar } from "primevue";

</script>

<template>
  <div>
    <pv-toolbar>
      <template #start>
        <div class="flex align-items-center">
          <img
              src="https://upload.wikimedia.org/wikipedia/commons/5/5e/Hogwartscrest.png"
              alt="Harry Potter Logo"
              style="height: 40px; margin-right: 10px;"
          />
          <h2 class="m-0">Harry Potter Fan Store</h2>
        </div>
      </template>

      <template #end>
        <pv-select-button
            v-model="$i18n.locale"
            :options="languages"
            option-label="label"
            option-value="value"
        />
      </template>
    </pv-toolbar>
  </div>
</template>

<style scoped>
h2 {
  font-size: 1.5rem;
  font-weight: bold;
}
</style>
