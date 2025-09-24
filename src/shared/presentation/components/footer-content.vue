<script setup lang="js">
import {useI18n} from "vue-i18n";

const { t } = useI18n();

</script>

<template>
  <div class="grid bg-green-400 mt-4 p-4 align-content-start">
    <div class="col-12 ml-3 align-items-center justify-content-center">
      <p>Copyright © 2025 Harry Potter Fan Store, inc All rights reserved.</p>
    </div>
    <div class="col-12 ml-3 mt-3 align-items-center justify-content-center">
      <p>
        {{t('footer.developed-by', {name: 'U202312348 Yazid Said Conde'})}}
      </p>
      <p>{{ t('footer.powered-by')}} <a href="https://www.newsapi.org">NewsAPI.org</a>
        {{ t('footer.and')}} <a href="https://www.clearbit.com">Clearbit Logo API</a>
      </p>
    </div>
  </div>
</template>

<style scoped>

</style>