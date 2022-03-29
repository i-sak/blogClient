<template>
  <footer
    class="footer"
    :class="{ [`footer-${type}`]: type }"
    :data-background-color="backgroundColor"
  >
    <div class="container">
      <nav>
        <ul>
          <li>
            <router-link to="/"><strong id="footerOwner"> ISAAC </strong></router-link>
          </li>
          <li>
            <a href="https://lifere.tistory.com/" target="_blank">Tistory</a>
            <!-- <a href="https://www.creative-tim.com">
              Creative Tim
            </a> -->
          </li>
          <li>
            <a href="https://blog.naver.com/isaac7263" target="_blank">Naver</a>
            <!-- <a href="https:///presentation.creative-tim.com">
              About Us
            </a> -->
          </li>
          <li>
            <a href="https://github.com/i-sak" target="_blank">Github</a>
            <!-- <a href="https:///blog.creative-tim.com">
              Blog
            </a> -->
          </li>
          <li>
            <a href="https://smartstore.naver.com/topperfriends" target="_blank">Topper Friends</a>
            <!-- <a href="https://www.creative-tim.com/license">
              Licenses
            </a> -->
          </li>
          <li>
            <router-link to="/componentsAll">componentsAll</router-link>
          </li>
          <li>
            <a href="https://demos.creative-tim.com/vue-material-kit/documentation/" target="_blank">DOCUMENTATION</a>
          </li>
        </ul>
      </nav>
      <!-- <div class="copyright">
        &copy; {{ year }}, made with <md-icon>favorite</md-icon> by
        <a href="https://www.creative-tim.com/" target="_blank">Creative Tim</a>
        for a better web.
      </div> -->
    </div>
  </footer>
</template>
<script>
export default {
  props: {
    backgroundColor: String,
    type: String
  },
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>
<style>
div.copyright,
div.copyright a,
div.copyright a:visited {
  color : #cccccc;
}
#footerOwner {
  font-weight: 900;
  font-size: 150%;
  color : #108b17;
  padding-right: 10px;
}
</style>
