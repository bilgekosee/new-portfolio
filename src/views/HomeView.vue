<template>
  <v-app id="home">
    <Navbar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Hello,</h1>
              <h1 class="text-white">I'M BİLGE KÖŞE</h1>
              <span class="text-grey"
                >Web Designer & Engineer of Mechatronics</span
              ><br />
              <v-btn title dark class="text-yellow mt-8" variant="outlined"
                >Contact Me</v-btn
              >
            </div>
          </v-col>
          <v-col cols="2">
            <div
              style="
                color: #f0a202;
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              "
              class="mt-16"
            >
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-img
                src="1.gif"
                style="
                  border-radius: 50%;
                  height: 250px;
                  width: 250px;
                  object-fit: cover;
                  left: 150px;
                  background: transparent;

                  border: 5px double yellowgreen;
                  border-color: #f0a202;
                "
              ></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img
                  src="2.jpg"
                  style="
                    margin-left: 0px;
                    margin-top: 50px;
                    width: 356px;
                    height: 300px;
                    border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
                  "
                  class=""
                ></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16">About Me</h5>
              <div style="width: 120px">
                <v-slider v-model="slider2" color="#F0A202"></v-slider>
              </div>
              <h4 class="mt-n4">I Am a Mechatronics Engineer</h4>
              <h4 class="">And Developer</h4>
              <p class="text-grey">
                Hello i am Bilge first of all welcome to my site. My main field
                is mechatronics engineering.However, since I found myself more
                successful in software, I turned to software for a long time,
                including my school life, and developed myself in the field of
                software.
              </p>
              <br />
              <p class="text-grey">
                Due to my field, I have seen many programming languages as
                courses at the university. For example,
                c,c++,c#,ROS,Matlab,Scilab,microprocessor based systems and
                coding(STM).Apart from programming, I am proficient in many
                drawing and design applications such as Autocad, SolidWorks,
                Catia.
              </p>
              <v-btn tile dark color="yellow" class="mt-4"
                >Download Resume</v-btn
              >
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>What Me Do?</h2>
        <div style="width: 120px; margin: 0 auto">
          <v-slider v-model="slider2" color="#F0A202"></v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn
                  icon="fas fa-laptop"
                  color="#E39774"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Web Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  I have designed many websites <br />with the help of html css
                  and javascript <br />
                  in the Vue.js environment.
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon="fa-solid fa-robot"
                  color="#E39774"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Robotics</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  I can do robotic coding using STM32CubeIDE.<br />
                  I coded my balance robot, <br />which is a graduation project
                  with this framework.
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon="fa-solid fa-plus-minus"
                  color="#E39774"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Maths</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  I can calculate value using controllers <br />
                  like PID and LQR for real time <br />and automatic control
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="yellow" class="mr-2">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Web Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Language</v-btn>
          <v-btn class="mr-2" variant="tonal">Robotics</v-btn>
          <v-btn variant="tonal">Maths</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" sm="4">
              <v-hover v-slot="{ isHovering, props }">
                <v-card
                  :elevation="isHovering ? 12 : 2"
                  :class="{ 'on-hover': isHovering }"
                  v-bind="props"
                >
                  <v-img :src="item.img" height="225px" cover> </v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="yellow" class="mt-4">Load More</v-btn>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4">
              <v-card class="md-auto" max-width="344" height="">
                <v-img src="10.jpg" height="218px" cover></v-img>
                <v-card-title>I'm here to do the best</v-card-title>
                <v-card-subtitle> By Bilge Köşe | 05 feb 2023 </v-card-subtitle>
                <v-card-test
                  >With my ability to learn quickly and adapt quickly, you can
                  be sure that I will strive to be the best by adding a new one
                  every day.</v-card-test
                >
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="md-auto" max-width="344" height="">
                <v-img src="g.png" height="218px" cover></v-img>
                <v-card-title>Check out the code i wrote</v-card-title>
                <v-card-subtitle> By Bilge Köşe | 05 feb 2023 </v-card-subtitle>
                <v-card-test
                  >You can find many code examples I wrote on Github, click the
                  link now</v-card-test
                >
                <br />
                <a href="https://github.com/bilgekosee">click for github</a>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="md-auto" max-width="344" height="">
                <v-img src="robot.jpg" height="218px" cover></v-img>
                <v-card-title>Balance Robot</v-card-title>
                <v-card-subtitle> By Bilge Köşe | 05 feb 2023 </v-card-subtitle>
                <v-card-test
                  >If you want to take a look at the balance robot I made for
                  the graduation project, click the link.</v-card-test
                >
                <br />
                <a href="https://disk.yandex.com.tr/d/p9p2Dx6TXtEI3A"
                  >Click to browser the project</a
                >
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" id="blog">
        <div class="hi">
          <v-row>
            <v-col cols="12" sm="8">
              <h1 class="mt-9">Hire me for your awesome project</h1>
              <p class="text-grey">
                Since I have 2 months of R&D experience, I have been in the
                construction of many projects. Apart from coding, I also have
                experience in R&D projects.
              </p>
            </v-col>
            <v-col cols="12" sm="4">
              <v-btn color="yellow" class="mt-15">Hire Me</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Contact info</h1>
              <v-btn
                icon="fas fa-map-marker-alt"
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption"
                >Eğriçam district 22103 street Yenişehir/Mersin/Turkey</span
              ><br />
              <v-btn
                icon="fas fa-phone-alt"
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">(+90) 507 084 ****</span><br />
              <v-btn
                icon="fas fa-envelope"
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">bilge.koosee@gmail.com</span><br />
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Send your message</h1>
            <v-divider></v-divider>
            <span class="text-caption"
              >If you think we can do a good job together, contact me now.</span
            >
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field
                  label="Name"
                  persistent-hint
                  variant="outlined"
                ></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field
                  label="Phone No"
                  persistent-hint
                  variant="outlined"
                ></v-text-field>
              </v-col>
            </v-row>
            <v-textarea
              label="Message"
              persistent-hint
              variant="outlined"
            ></v-textarea>
            <v-btn color="yellow" class="mt-2">Submit Now</v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView />
  </v-app>
</template>

<script>
import { defineComponent } from "vue";

// Components
import Navbar from "../components/Navbar.vue";
import FooterView from "../components/FooterView.vue";

export default defineComponent({
  name: "HomeView",
  setup() {
    return {
      slider2: 50,

      items: [
        {
          img: "3.jpg",
        },
        {
          img: "4.jpg",
        },
        {
          img: "5.jpg",
        },
        {
          img: "6.jpg",
        },
        {
          img: "7.jpg",
        },
        {
          img: "girl.gif",
        },
      ],
    };
  },

  components: {
    Navbar,
    FooterView,
  },
});
</script>
<style scoped>
.v-container {
  padding: 16px 0;
}
.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: #134a5b;
}

.head:before {
  content: " ";
  position: absolute;
  font-family: Impact, Haettenschweiler, "Arial Narrow Bold", sans-serif;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: #004643;
  transform: skew(0deg, 6deg);
}
.head:after {
  content: " ";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: #0f3735;
  transform: skew(0deg, -6deg);
}
.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #002844;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}
.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-left: 8px;
}
.imgHover {
  padding: 0 200px;
}
.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f0a202;
}
.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #002844;
  margin-top: -24px;
}
</style>
