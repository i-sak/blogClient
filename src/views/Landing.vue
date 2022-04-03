<template>
  <div class="wrapper">
    <parallax class="section page-header header-filter" :style="headerStyle">
      <div class="container">
        <div class="md-layout">
          <div
            class="md-layout-item md-size-50 md-small-size-70 md-xsmall-size-100"
          >
            <h1 class="title">Isaac's Story</h1>
            <h4>
              Nice to meet you. This is my portfolio website.
              <!-- Every landing page needs a small description after the big bold
              title, that's why we added this text here. Add here all the
              information that can make you or your product create the first
              impression. -->
            </h4>
            <br />
            <md-button
              href="https://www.youtube.com/channel/UCpnu38d9yOk8rXhVb_Dc_5g"
              class="md-success md-lg"
              target="_blank">
              <i class="fas fa-play"></i> 
              Watch video
            </md-button>
          </div>
        </div>
      </div>
    </parallax>
    <div class="main main-raised">
      <div class="section">
        <div class="container">
          <div class="md-layout">
            <div
              class="md-layout-item md-size-66 md-xsmall-size-100 mx-auto text-center"
            >
              <h2 class="title text-center">Portfolio</h2>
              <h5 class="description">
                I like to study development and computer science.I created this
                website to show documents and works produced while researching
                This site contains blog and bulletin board features.
                <!-- This is the paragraph where you can write more details about
                your product. Keep you user engaged by providing meaningful
                information. Remember that by this time, the user is curious,
                otherwise he wouldn't scroll to get here. Add a button if you
                want the user to see more. -->
              </h5>
            </div>
          </div>
          <div class="features text-center">
            <div class="md-layout">
              <!-- <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="info">
                  <div class="icon icon-info">
                    <md-icon>chat</md-icon>
                  </div>
                  <h4 class="info-title">Free Chat</h4>
                  <p>
                    Divide details about your product or agency work into parts.
                    Write a few lines about each one. A paragraph describing a
                    feature will be enough.
                  </p>
                </div>
              </div> -->
              <!-- <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="info">
                  <div class="icon icon-success">
                    <md-icon>verified_user</md-icon>
                  </div>
                  <h4 class="info-title">Verified Users</h4>
                  <p>
                    Divide details about your product or agency work into parts.
                    Write a few lines about each one. A paragraph describing a
                    feature will be enough.
                  </p>
                </div>
              </div> -->
              <!-- <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="info">
                  <div class="icon icon-danger">
                    <md-icon>fingerprint</md-icon>
                  </div>
                  <h4 class="info-title">Fingerprint</h4>
                  <p>
                    Divide details about your product or agency work into parts.
                    Write a few lines about each one. A paragraph describing a
                    feature will be enough.
                  </p>
                </div>
              </div> -->
            </div>
          </div>
        </div>
      </div>
      <div class="section text-center">
        <div class="container">
          <h2 class="title">Creator</h2>
          <div class="team">
            <div class="md-layout">
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <!-- <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        :src="teamImg1"
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      />
                    </div>
                    <h4 class="card-title">
                      ???
                      <br />
                      <small class="card-description text-muted">Model</small>
                    </h4>

                    <md-card-content>
                      <p class="card-description">
                        You can write here details about one of your team
                        members. You can give more details about what they do.
                        Feel free to add some <a href="#">links</a> for people
                        to be able to follow them outside the site.
                      </p>
                    </md-card-content>

                    <md-card-actions class="text-center">
                      <md-button
                        href="javascript:void(0)"
                        class="md-just-icon md-simple"
                      >
                        <i class="fab fa-twitter"></i>
                      </md-button>
                      <md-button
                        href="javascript:void(0)"
                        class="md-just-icon md-simple"
                      >
                        <i class="fab fa-instagram"></i>
                      </md-button>
                      <md-button
                        href="javascript:void(0)"
                        class="md-just-icon md-simple"
                      >
                        <i class="fab fa-facebook-square"></i>
                      </md-button>
                    </md-card-actions>
                  </md-card>
                </div> -->
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        :src="teamImg2"
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      />
                    </div>
                    <h4 class="card-title">
                      Isaac Kim
                      <br />
                      <small class="card-description text-muted"
                        >Developer</small
                      >
                    </h4>

                    <md-card-content>
                      <p class="card-description">
                        
                        I love researching computer science and development, so I am constantly studying and documenting what I have studied. I'm Isaac Kim, a growing developer.
                        <br><br>
                        컴퓨터 과학과 개발을 연구하는 것을 좋아해서
                        끊임없이 공부하고, 공부한 것을 기록하고 있습니다.
                        성장하는 개발자 김이삭 입니다.
                        <!-- You can write here details about one of your team
                        members. You can give more details about what they do.
                        Feel free to add some <a href="#">links</a> for people
                        to be able to follow them outside the site. -->
                      </p>
                    </md-card-content>

                    <md-card-actions class="text-center">
                      <!-- <md-button
                        href="javascript:void(0)"
                        class="md-just-icon md-simple"
                      >
                        <i class="fab fa-twitter"></i>
                      </md-button>
                      <md-button
                        href="javascript:void(0)"
                        class="md-just-icon md-simple"
                      >
                        <i class="fab fa-linkedin"></i>
                      </md-button> -->

                     <md-button
                        href="https://lifere.tistory.com/"
                        class="md-just-icon md-simple"
                        target="_blank"
                      >
                        <i class="fab fa-blogger"></i>
                      </md-button>

                      <md-button
                        href="https://github.com/i-sak"
                        class="md-just-icon md-simple"
                        target="_blank"
                      >
                        <i class="fab fa-github"></i>
                      </md-button>

                      <md-button
                        href="https://blog.naver.com/isaac7263"
                        class="md-just-icon md-simple"
                        target="_blank"
                      >
                        <i class="fab fa-blogger"></i>
                      </md-button>
                      
                      <!-- javascript:void(0) -->
                      <md-button
                        href="https://www.instagram.com/isaac.kim.dev/"
                        class="md-just-icon md-simple"
                        target="_blank"
                      >
                        <i class="fab fa-instagram"></i>
                      </md-button>
                      
                      <md-button
                        href="https://www.facebook.com/profile.php?id=100003562823035"
                        class="md-just-icon md-simple"
                        target="_blank"
                      >
                        <i class="fab fa-facebook-square"></i>
                      </md-button>
                    </md-card-actions>
                  </md-card>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <!-- <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        :src="teamImg3"
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      />
                    </div>
                    <h4 class="card-title">
                      ???
                      <br />
                      <small class="card-description text-muted">Model</small>
                    </h4>

                    <md-card-content>
                      <p class="card-description">
                        You can write here details about one of your team
                        members. You can give more details about what they do.
                        Feel free to add some <a href="#">links</a> for people
                        to be able to follow them outside the site.
                      </p>
                    </md-card-content>

                    <md-card-actions class="text-center">
                      <md-button
                        href="javascript:void(0)"
                        class="md-just-icon md-simple"
                      >
                        <i class="fab fa-twitter"></i>
                      </md-button>
                      <md-button
                        href="javascript:void(0)"
                        class="md-just-icon md-simple"
                      >
                        <i class="fab fa-instagram"></i>
                      </md-button>
                      <md-button
                        href="javascript:void(0)"
                        class="md-just-icon md-simple"
                      >
                        <i class="fab fa-facebook-square"></i>
                      </md-button>
                    </md-card-actions>
                  </md-card>
                </div> -->
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- <div class="alert alert-success">
        <div class="container">
          <button
            type="button"
            aria-hidden="true"
            class="close"
            @click="event => removeNotify(event, 'alert-success')"
          >
            <md-icon>clear</md-icon>
          </button>
          <div class="alert-icon">
            <md-icon>check</md-icon>
          </div>

          <b> SUCCESS ALERT </b> : Isaac님께 메일 전송 완료!
        </div>
      </div> -->

      <div class="section section-contacts">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-66 md-xsmall-size-100 mx-auto">
              <h2 class="text-center title">Work with me</h2>
              <h4 class="text-center description">
                Contact me. We will get back to you in a few hours.
                <!-- Divide details about your product or agency work into parts.
                Write a few lines about each one and contact us about any
                further collaboration. We will responde get back to you in a
                couple of hours. -->
              </h4>
              <form class="contact-form"
                @submit.prevent="sendEmail">
                <div class="md-layout">
                  <div class="md-layout-item md-size-50">
                    <md-field>
                      <label>Your Name</label>
                      <md-input v-model="name" type="text" ref="name"></md-input>
                    </md-field>
                  </div>
                  <div class="md-layout-item md-size-50">
                    <md-field>
                      <label>Your Email</label>
                      <md-input v-model="email" type="email" ref="email"></md-input>
                    </md-field>
                  </div>
                </div>
                <md-field maxlength="5">
                  <label>Your Message</label>
                  <md-textarea v-model="message" ref="message"></md-textarea>
                </md-field>
                <div class="md-layout">
                  <div class="md-layout-item md-size-33 mx-auto text-center">
                    <md-button type="submit" class="md-success">Send Message</md-button>
                  </div>
                </div>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import emailjs from '@emailjs/browser';
import{ init } from '@emailjs/browser';
var initVar;
init("AjU_EyRvJpHTVZH3b");

export default {
  bodyClass: "landing-page",
  props: {
    header: {
      type: String,
      default: require("@/assets/img/bg7.jpg")
    },

    teamImg1: {
      type: String,
      default: require("@/assets/img/faces/silhouette1.png")
    },
    teamImg2: {
      type: String,
      default: require("@/assets/img/faces/isak.jpg")
    },
    teamImg3: {
      type: String,
      default: require("@/assets/img/faces/silhouette2.png")
    }
  },
  data() {
    return {
      name: null,
      email: null,
      message: null,
    };
  },
  methods: {
    sendEmail() {
      if (!this.checkFormInputForContactMe()) return;
      
      var obj = {
        to_name : 'isaac',
        from_name : this.name,
        email :  this.email,
        message :  this.message
      }
      emailjs.send('service_czngeek', 'template_5x2iinb', obj)
        .then((result) => {
            console.log('SUCCESS!', result.text);
            this.name = ''
            this.email = ''
            this.message = ''
            alert('Isaac님께 메일 전송 완료!');
        }, (error) => {
            console.log('FAILED...', error.text);
        });
    },

    removeNotify(e, notifyClass) {
      var target = e.target;
      while (target.className.indexOf(notifyClass) === -1) {
        target = target.parentNode;
      }
      return target.parentNode.removeChild(target);
    },

    // [CHECK] Form input for Contact me 
    checkFormInputForContactMe() {
      if(this.name == '' || this.name == null) {
        alert('Name을 입력해주세요.');
        this.$refs.name.$el.focus()
        return false;
      } else if (this.email == '' || this.email == null) {
        alert('Email을 입력해주세요.');
        this.$refs.email.$el.focus()
        return false;
      } else if (this.message == '' || this.message == null) {
        alert('Message를 입력해주세요.');
        this.$refs.message.$el.focus()
        return false;
      } else return true;
    }

  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`
      };
    }
  }
};
</script>

<style lang="scss" scoped>
.md-card-actions.text-center {
  display: flex;
  justify-content: center !important;
}
.contact-form {
  margin-top: 30px;
}

.md-has-textarea + .md-layout {
  margin-top: 15px;
}
</style>
