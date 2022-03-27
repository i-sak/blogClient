<template>
  <div id="material-kit">
    <div :class="{ 'nav-open': NavbarStore.showNavbar }">
      
      <!-- <a href="./layout/MainNavbar.vue"></a> -->
      <router-view name="header" />

      <div>
        <router-view />
      </div>

      <!-- <a href="./layout/MainFooter.vue"></a> -->
      <router-view name="footer" />
    </div>
  </div>
</template>
