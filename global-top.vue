<template>
  <footer 
  v-if="$slidev.nav.currentPage == 1 || 
  $slidev.nav.currentPage == 3 || 
  $slidev.nav.currentPage == 7 || 
  $slidev.nav.currentPage == 10 || 
  $slidev.nav.currentPage == 15 || 
  $slidev.nav.currentPage == 23 ||
  $slidev.nav.currentPage == 27 ||
  $slidev.nav.currentPage == 33 ||
   $slidev.nav.currentPage == 36
  "
  class="absolute top-0 left-0">
    <img src="/images/title.PNG" />
  </footer>
</template>