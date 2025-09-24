<script setup lang="js">
import { ref, onMounted } from "vue";
import { Card as PvCard } from "primevue";

const books = ref([]);

// Imagen de placeholder por si no hay cover
const placeholder = "https://via.placeholder.com/300x400?text=No+Image";


onMounted(async () => {
  try {
    const res = await fetch("https://potterapi-fedeperin.vercel.app/es/books");
    books.value = await res.json();
  } catch (error) {
    console.error("Error al cargar libros:", error);
  }
});
</script>

<template>
  <div class="p-4">
    <h2 class="mb-4">Library Books</h2>

    <div class="grid">
      <div v-for="book in books" :key="book.id" class="col-12 md:col-4">
        <pv-card class="m-2 shadow-2">
          <!-- Imagen -->
          <template #header>
            <img
                :src="book.cover || placeholder"
                :alt="book.title"
                class="w-full h-64 object-cover"
            />
          </template>

          <!-- Título -->
          <template #title>
            {{ book.title }}
          </template>

          <!-- Título original -->
          <template #subtitle>
            <em>{{ book.originalTitle }}</em>
          </template>

          <!-- Contenido -->
          <template #content>
            <p class="mb-2">{{ book.description }}</p>
            <p><strong>Pages:</strong> {{ book.pages }}</p>
          </template>
        </pv-card>
      </div>
    </div>
  </div>
</template>

<style scoped>
h2 {
  font-size: 1.5rem;
  font-weight: bold;
}
</style>
