<script setup lang="js">
import LanguageSwitcher from "./language-switcher.vue";
import {Toolbar as PvToolbar} from "primevue";
import FooterContent from "./footer-content.vue";
import LibraryBooks from "./library-books.vue";
</script>
<template>
  <div>
    <div>
      <pv-toolbar>
        <template #start>
          <div class="flex align-items-center">
            <img src="https://upload.wikimedia.org/wikipedia/commons/5/5e/Hogwartscrest.png"
                 alt="Harry Potter Logo"
                 style="height: 40px; margin-right: 10px;"
                 />
            <h2 class="m-0">Harry Potter Fan Store</h2>
          </div>
        </template>

         <template #end>
        <language-switcher></language-switcher>
           <a href="https://www.crisol.com.pe" target="_blank" >
             <pv-button
                 label="Search Harry Potter Books"
                 icon = "pi pi-search"
                 class="ml-2"
             />
           </a>
      </template>
      </pv-toolbar>
    </div>
  </div>
  <library-books />
  <footer-content/>
</template>
<style scoped>
h2 {
  font-size: 1.5rem;
  font-weight: bold;
}
</style>