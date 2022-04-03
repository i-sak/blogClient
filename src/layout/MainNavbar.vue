<template>
  <md-toolbar
    id="toolbar"
    md-elevation="0"
    class="md-transparent md-absolute"
    :class="extraNavClasses"
    :color-on-scroll="colorOnScroll"
  >
    <div class="md-toolbar-row md-collapse-lateral">
      <div class="md-toolbar-section-start">
        <h3 class="md-title" id="mainHeaderTitle"><router-link to="/">ISAAC WORLD</router-link></h3>
      </div>
      <div class="md-toolbar-section-end">
        <md-button
          class="md-just-icon md-simple md-toolbar-toggle"
          :class="{ toggled: toggledClass }"
          @click="toggleNavbarMobile()"
        >
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </md-button>

        <div class="md-collapse">
          <div class="md-collapse-wrapper">
            <mobile-menu nav-mobile-section-start="false">
              <!-- Here you can add your items from the section-start of your toolbar -->
            </mobile-menu>
            <md-list>

              <!-- <li class="md-list-item" v-if="!showDownload">
                <a
                  href="javascript:void(0)"
                  class="md-list-item-router md-list-item-container md-button-clean dropdown"
                >
                  <div class="md-list-item-content">
                    <drop-down direction="down">
                      <md-button
                        slot="title"
                        class="md-button md-button-link md-white md-simple dropdown-toggle"
                        data-toggle="dropdown"
                      >
                        <i class="material-icons">apps</i>
                        <p>Components</p>
                      </md-button>
                      <ul class="dropdown-menu dropdown-with-icons">
                        <li>
                          <a href="#/componentsAll">
                            <i class="material-icons">layers</i>
                            <p>All Components</p>
                          </a>
                        </li>
                        <li>
                          <a
                            href="https://demos.creative-tim.com/vue-material-kit/documentation/"
                          >
                            <i class="material-icons">content_paste</i>
                            <p>Documentation</p>
                          </a>
                        </li>
                      </ul>
                    </drop-down>
                  </div>
                </a>
              </li> -->

              <!-- top menu navigator -->
              
              <!-- href="/"
                target="_blank"
                속성 제거 
                 -->
              <md-list-item v-if="showDownload">
                <p class="menuList">
                  <router-link to="/landing">Landing Page</router-link>
                </p>
              </md-list-item>

              <md-list-item v-if="showDownload">
                <p class="menuList">
                  <router-link to="/profile">Profile</router-link>
                </p>
              </md-list-item>

              <md-list-item v-if="showDownload">
                <p class="menuList">
                  <router-link to="/login">Login</router-link>
                </p>
              </md-list-item>

              <md-list-item v-if="showDownload">
                <p class="menuList">
                  <a href="https://github.com/i-sak" target="_blank">Github</a>
                </p>
              </md-list-item>

              <!-- Document 개발 문서 -->
              <!-- <md-list-item
                href="https://demos.creative-tim.com/vue-material-kit/documentation/"
                target="_blank"
                v-if="showDownload"
              >
                <i class="material-icons">content_paste</i>
                <p>Documentation</p>
              </md-list-item> -->

              <!-- 화면 최하단으로 이동 -->
              <!-- <md-list-item
                href="javascript:void(0)"
                @click="scrollToElement()"
                v-if="showDownload"
              >
                <i class="material-icons">cloud_download</i>
                <p>Download</p>
              </md-list-item> -->

              <li class="md-list-item" v-else>
                <a
                  href="javascript:void(0)"
                  class="md-list-item-router md-list-item-container md-button-clean dropdown"
                >
                  <div class="md-list-item-content">
                    <drop-down direction="down">
                      <md-button
                        slot="title"
                        class="md-button md-button-link md-white md-simple dropdown-toggle"
                        data-toggle="dropdown"
                      >
                        <i class="material-icons">view_carousel</i>
                        <p>Pages</p>
                      </md-button>
                      <ul class="dropdown-menu dropdown-with-icons">
                        <li>
                          <a href="#/landing">
                            <i class="material-icons">view_day</i>
                            <p>Landing Page</p>
                          </a>
                        </li>
                        <li>
                          <a href="#/login">
                            <i class="material-icons">fingerprint</i>
                            <p>Login Page</p>
                          </a>
                        </li>
                        <li>
                          <a href="#/profile">
                            <i class="material-icons">account_circle</i>
                            <p>Profile Page</p>
                          </a>
                        </li>
                      </ul>
                    </drop-down>
                  </div>
                </a>
              </li>
              
              <li class="md-list-item" v-if="!showDownload">
                <a
                  href="javascript:void(0)"
                  class="md-list-item-router md-list-item-container md-button-clean dropdown"
                >
                <div class="md-list-item-content">
                    <drop-down direction="down">
                      <md-button
                        slot="title"
                        class="md-button md-button-link md-white md-simple dropdown-toggle"
                        data-toggle="dropdown"
                      >
                        <i class="material-icons">category</i>
                        <p>Blog Category</p>
                      </md-button>
                      <ul class="dropdown-menu dropdown-with-icons">
                        <!-- blogTypeArray -->
                        <li v-for="(a, i) in blogTypeArray" :key="i">
                          <router-link
                            :to="{ path: `/blog`, query: { title: a } }"
                          >
                            {{ a }}
                          </router-link>
                          <!-- <a :href="'#/board?subject='+a">
                            <i class="material-icons">article</i>
                            <p>{{a}}</p>
                          </a> -->
                        </li>

                        <!-- <li>
                          <a href="#/board?subject=자유게시판">
                            <i class="material-icons">article</i>
                            <p>자유게시판</p>
                          </a>
                        </li>
                        
                        <li>
                          
                          <a href="#/login"> 
                            <i class="material-icons">article</i>
                            <p>login</p>
                          </a>
                        </li>
                        <li>
                          
                          <a href="#/profile">
                            <i class="material-icons">article</i>
                            <p>profile</p>
                          </a>
                        </li> -->
                      </ul>
                    </drop-down>
                  </div>
                </a>
              </li>

              <li class="md-list-item" v-if="!showDownload">
                <a
                  href="javascript:void(0)"
                  class="md-list-item-router md-list-item-container md-button-clean dropdown"
                >
                <div class="md-list-item-content">
                    <drop-down direction="down">
                      <md-button
                        slot="title"
                        class="md-button md-button-link md-white md-simple dropdown-toggle"
                        data-toggle="dropdown"
                      >
                        <i class="material-icons">category</i>
                        <p>BOARD Category</p>
                      </md-button>
                      <ul class="dropdown-menu dropdown-with-icons">

                        <!-- boardTypeArray -->
                        <li v-for="(a, i) in boardTypeArray" :key="i">
                          <router-link :to="{path : `/board`, query :{title : a}}"> 
                          {{a}}
                          </router-link>
                          <!-- <a :href="'#/board?subject='+a">
                            <i class="material-icons">article</i>
                            <p>{{a}}</p>
                          </a> -->
                        </li>

                        <!-- <li>
                          <a href="#/board?subject=자유게시판">
                            <i class="material-icons">article</i>
                            <p>자유게시판</p>
                          </a>
                        </li>
                        
                        <li>
                          
                          <a href="#/login"> 
                            <i class="material-icons">article</i>
                            <p>login</p>
                          </a>
                        </li>
                        <li>
                          
                          <a href="#/profile">
                            <i class="material-icons">article</i>
                            <p>profile</p>
                          </a>
                        </li> -->
                      </ul>
                    </drop-down>
                  </div>
                </a>
              </li>

              <!-- 트위터 -->
              <!-- <md-list-item
                href="https://twitter.com/CreativeTim"
                target="_blank"
              >
                <i class="fab fa-twitter"></i>
                <p class="hidden-lg">Twitter</p>
                <md-tooltip md-direction="bottom"
                  >Follow us on Twitter</md-tooltip
                >
              </md-list-item> -->
              
              <!-- 페이스북 -->
              <!-- <md-list-item
                href="https://www.facebook.com/CreativeTim"
                target="_blank"
              >
                <i class="fab fa-facebook-square"></i>
                <p class="hidden-lg">Facebook</p>
                <md-tooltip md-direction="bottom"
                  >Like us on Facebook</md-tooltip
                >
              </md-list-item> -->

              <!-- 인스타그램 -->
              <!-- <md-list-item
                href="https://www.instagram.com/CreativeTimOfficial"
                target="_blank"
              >
                <i class="fab fa-instagram"></i>
                <p class="hidden-lg">Instagram</p>
                <md-tooltip md-direction="bottom"
                  >Follow us on Instagram</md-tooltip
                >
              </md-list-item> -->

            </md-list>
          </div>
        </div>
      </div>
    </div>
  </md-toolbar>
</template>

<script>
let resizeTimeout;
function resizeThrottler(actualResizeHandler) {
  // ignore resize events as long as an actualResizeHandler execution is in the queue
  if (!resizeTimeout) {
    resizeTimeout = setTimeout(() => {
      resizeTimeout = null;
      actualResizeHandler();

      // The actualResizeHandler will execute at a rate of 15fps
    }, 66);
  }
}

import MobileMenu from "@/layout/MobileMenu";
export default {
  components: {
    MobileMenu
  },
  props: {
    type: {
      type: String,
      default: "white",
      validator(value) {
        return [
          "white",
          "default",
          "primary",
          "danger",
          "success",
          "warning",
          "info"
        ].includes(value);
      }
    },
    colorOnScroll: {
      type: Number,
      default: 0
    }
  },
  
  // data
  data() {
    return {
      extraNavClasses: "",
      toggledClass: false,
      blogTypeArray: ["Vue.js", "Java", "Database"],
      boardTypeArray: ["자유게시판"]
    };
  },
  computed: {
    // Index 메뉴가 아닌 MenuList 보여주기
    showDownload() {
      const excludedRoutes = [
        "login",
        "landing",
        "profile",
        "blog",
        "board",
        "boardWrite"
      ];
      return excludedRoutes.every(r => r !== this.$route.name);
    }
  },
  methods: {
    bodyClick() {
      let bodyClick = document.getElementById("bodyClick");

      if (bodyClick === null) {
        let body = document.querySelector("body");
        let elem = document.createElement("div");
        elem.setAttribute("id", "bodyClick");
        body.appendChild(elem);

        let bodyClick = document.getElementById("bodyClick");
        bodyClick.addEventListener("click", this.toggleNavbarMobile);
      } else {
        bodyClick.remove();
      }
    },
    toggleNavbarMobile() {
      this.NavbarStore.showNavbar = !this.NavbarStore.showNavbar;
      this.toggledClass = !this.toggledClass;
      this.bodyClick();
    },
    handleScroll() {
      let scrollValue =
        document.body.scrollTop || document.documentElement.scrollTop;
      let navbarColor = document.getElementById("toolbar");
      this.currentScrollValue = scrollValue;
      if (this.colorOnScroll > 0 && scrollValue > this.colorOnScroll) {
        this.extraNavClasses = `md-${this.type}`;
        navbarColor.classList.remove("md-transparent");
      } else {
        if (this.extraNavClasses) {
          this.extraNavClasses = "";
          navbarColor.classList.add("md-transparent");
        }
      }
    },
    scrollListener() {
      resizeThrottler(this.handleScroll);
    },
    scrollToElement() {
      let element_id = document.getElementById("downloadSection");
      if (element_id) {
        element_id.scrollIntoView({ block: "end", behavior: "smooth" });
      }
    }
  },
  mounted() {
    document.addEventListener("scroll", this.scrollListener);
  },
  beforeDestroy() {
    document.removeEventListener("scroll", this.scrollListener);
  }
};
</script>
<style lang="css">
  h3#mainHeaderTitle a {
    font-weight: bold;
    color :#cccccc;
  }
  p.menuList {
    padding-top: 1vh;
  }
</style>