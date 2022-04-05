<template>
  <div class="wrapper">
    <parallax class="page-header header-filter" :style="headerStyle">
      <div class="md-layout">
        <div class="md-layout-item">
          <div class="image-wrapper">
            <img :src="leaf4" alt="leaf4" class="leaf4" v-show="leafShow" />
            <img :src="leaf3" alt="leaf3" class="leaf3" v-show="leafShow" />
            <img :src="leaf2" alt="leaf2" class="leaf2" v-show="leafShow" />
            <img :src="leaf1" alt="leaf1" class="leaf1" v-show="leafShow" />
            <div class="brand">
              <h2 id="title">{{ $route.query.title }}</h2>
              <h3>Board</h3>
            </div>
          </div>
        </div>
      </div>
    </parallax>
    <div class="main main-raised">
      <!-- <div class="section">
        <div class="container text-center">
          <div class="md-layout">
            <div
              class="md-layout-item md-size-66 md-xsmall-size-100 ml-auto mr-auto text-center"
            >
              <h2>Completed with examples</h2>
              <h4>
                The kit comes with three pre-built pages to help you get started
                faster. You can change the text and images and you're good to
                go. More importantly, looking at them will give you a picture of
                what you can built with this powerful kit.
              </h4>
            </div>
          </div>
        </div>
      </div> -->

      <div class="section section-basic">
        <div class="container">
          <div class="title">
            <h3>{{ this.$route.query.title }} 목록</h3>
            <div class="boardButtonSpace">
              <md-button class="md-primary md-round" @click="movePageBoardWrite"
                >글쓰기</md-button
              >
            </div>
          </div>
          <div class="md-layout">
            <div
              class="md-layout-item md-size-100 md-xsmall-size-100 ml-auto mr-auto text-left"
            >
              <table border="1">
                <tr
                  v-for="(a, i) in 5"
                  :key="i"
                  class="boardListRow"
                  @click="movePageBoardView(i)"
                >
                  <td class="boardListRowRightTd">
                    <div class="boardRowDetailTitle">
                      <h4>
                        <strong>자유게시판 제목 입니다. TEST TEST TEST</strong>
                      </h4>
                    </div>
                    <div class="boardRowDetailContents">
                      <p>
                        내용 미리보기 TEST TEST TEST TEST TEST TEST TEST
                      </p>
                    </div>
                    <div class="boardRowDetailInfo">
                      <p>김이삭 2022.04.01</p>
                    </div>
                  </td>
                  <td class="boardListRowLeftTd">
                    <img :src="imageTest" alt="imageTest" />
                  </td>
                </tr>
              </table>

              <!-- Pagination start-->
              <div id="pagination" class="md-layout-item md-xsmall-size-100">
                <span class="prevNextButton" @click="prevPagination">prev</span>
                <pagination
                  no-arrows
                  v-model="defaultPagination"
                  :page-count="5"
                >
                </pagination>
                <span class="prevNextButton" @click="nextPagination">next</span>
              </div>
              <!-- Pagination end -->
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Pagination } from "@/components";

export default {
  components: {
    Pagination
  },
  name: "board",
  bodyClass: "index-page",
  props: {
    image: {
      type: String,
      default: require("@/assets/img/vue-mk-header.jpg")
    },
    leaf4: {
      type: String,
      default: require("@/assets/img/leaf4.png")
    },
    leaf3: {
      type: String,
      default: require("@/assets/img/leaf3.png")
    },
    leaf2: {
      type: String,
      default: require("@/assets/img/leaf2.png")
    },
    leaf1: {
      type: String,
      default: require("@/assets/img/leaf1.png")
    },
    signup: {
      type: String,
      default: require("@/assets/img/city.jpg")
    },
    landing: {
      type: String,
      default: require("@/assets/img/landing.jpg")
    },
    profile: {
      type: String,
      default: require("@/assets/img/profile.jpg")
    }
  },
  data() {
    return {
      firstname: null,
      email: null,
      password: null,
      leafShow: false,
      subject: "Category",
      imageTest: require("@/assets/img/faces/isak.jpg"),
      // Pagination
      defaultPagination: 1
    };
  },
  methods: {
    leafActive() {
      if (window.innerWidth < 768) {
        this.leafShow = false;
      } else {
        this.leafShow = true;
      }
    },
    movePageBoardWrite() {
      this.$router.push({
        name: "boardWrite", params: { category: this.$route.query.title }
      });
    },
    movePageBoardView() {
      this.$router.push({
        name: "boardView", params: {}
      })
    },
    prevPagination() {
      if (this.defaultPagination <= 1) return;
      this.defaultPagination -= 1;
    },
    nextPagination() {
      this.defaultPagination += 1;
    }

  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.image})`
      };
    },
    signupImage() {
      return {
        backgroundImage: `url(${this.signup})`
      };
    }
  },
  mounted() {
    // let url = window.location.hash;
    // console.log(url)
    this.leafActive();
    window.addEventListener("resize", this.leafActive);
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.leafActive);
  }
};
</script>
<style lang="scss">
.section-download {
  .md-button + .md-button {
    margin-left: 5px;
  }
}

@media all and (min-width: 991px) {
  .btn-container {
    display: flex;
  }
  .brand #title {
    font-size: 500%;
  }
}
/** header title */
.brand #title {
  font-weight: bold;
}

/** 목록관련 */
table {
  border-collapse: collapse;
  border-top: 0px solid white;
  border-left: 0px solid white;
  border-right: 0px solid white;
  border-bottom: 1px solid lightgray;
}
.boardListRow {
  word-break: break-all;
}
.boardListRow:hover {
  background: linear-gradient(white, #fff9ff);
}
.boardListRowRightTd {
  width: 88vw;
}
.boardListRowLeftTd {
  width: 12vw;
}
.boardRowDetailTitle h4,
.boardRowDetailContents p,
.boardRowDetailInfo p {
  margin: 0;
  padding: 0;
}
.boardButtonSpace {
  text-align: right;
}
div#pagination {
  display: flex;
  justify-content: center;
}
span.prevNextButton {
  padding: 2px;
  padding-left: 10px;
  padding-right: 10px;
  margin: auto;
  color: white;
  border-radius: 40%;
  background-color: var(--md-theme-default-primary-on-background, #9c27b0);
  cursor: pointer;
}
</style>
