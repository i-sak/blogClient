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
            <strong id="footerOwner"> Isaac's </strong>
          </li>
          <li>
            <a href="https://lifere.tistory.com/">Tistory</a>
            <!-- <a href="https://www.creative-tim.com">
              Creative Tim
            </a> -->
          </li>
          <li>
            <a href="https://blog.naver.com/isaac7263">Naver</a>
            <!-- <a href="https:///presentation.creative-tim.com">
              About Us
            </a> -->
          </li>
          <li>
            <a href="https://github.com/i-sak">Github</a>
            <!-- <a href="https:///blog.creative-tim.com">
              Blog
            </a> -->
          </li>
          <li>
            <a href="https://smartstore.naver.com/topperfriends">Topper Friends</a>
            <!-- <a href="https://www.creative-tim.com/license">
              Licenses
            </a> -->
          </li>
          <li>
            <router-link to="/componentsAll">componentsAll</router-link>
          </li>
        </ul>
      </nav>
      <div class="copyright">
        &copy; {{ year }}, made with <md-icon>favorite</md-icon> by
        <a href="https://www.creative-tim.com/" target="_blank">Creative Tim</a>
        for a better web.
      </div>
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
.copyright {
  color : #c9c9c9;
}
.copyright a:visited {
  color : #c9c9c9;
}
#footerOwner {
  font-weight: 900;
  font-size: 150%;
  color : #108b17;
  padding-right: 10px;
}
</style>
