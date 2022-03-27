<template>
  <div id="home">
    <div class="static">
      <h1 class="title">Milla의 인생이야기</h1>
      <h1 class="final_title">감사합니다</h1>
      <div class="sky" :style="{ backgroundColor }">
        <ul class="clouds">
          <li class="cloud first_cloud">
            <img src="/images/cloud5.png" alt="" />
          </li>
          <li class="cloud first_cloud">
            <img src="/images/cloud6.png" alt="" />
          </li>
          <li class="cloud second_cloud">
            <img src="/images/cloud7.png" alt="" />
          </li>
        </ul>
        <ul class="first_village">
          <li class="ville" style="--left: 1; --scale: 20">
            <img src="/images/maincity.svg" alt="" />
          </li>
        </ul>
        <ul class="second_village">
                    <li class="ville" style="--left: 2; --scale: 4">
            <img src="/images/theatre.png" alt="" />
          </li>
          <li class="ville" style="--left: 15; --scale: 4">
            <img src="/images/museum.png" alt="" />
          </li>
          <li class="ville" style="--left: 6; --scale: 4">
            <img src="/images/cinema.png" alt="" />
          </li>
          <li class="ville" style="--left: 10; --scale: 5">
            <img src="/images/airport.png" alt="" />
          </li>
        </ul>
        <ul class="third_village">
          <li class="ville" style="--left: -1; --scale: 6">
            <img src="/images/city1.svg" alt="" />
          </li>
          <li class="ville" style="--left: 2; --scale: 5">
            <img src="/images/city2.svg" alt="" />
          </li>
          <li class="ville" style="--left: 4; --scale: 6">
            <img src="/images/city2.svg" alt="" />
          </li>
          <li class="ville" style="--left: 5; --scale: 6">
            <img src="/images/city1.svg" alt="" />
          </li>
          <li class="ville" style="--left: 5.5; --scale: 2">
            <img src="/images/house.png" alt="" />
          </li>
          <li class="ville" style="--left: 8; --scale: 6">
            <img src="/images/city1.svg" alt="" />
          </li>
          <li class="ville" style="--left: 13; --scale: 5">
            <img src="/images/city2.svg" alt="" />
          </li>
                    <li class="ville" style="--left: 15; --scale: 2">
            <img src="/images/house.png" alt="" />
          </li>
                    <li class="ville" style="--left: 15; --scale: 6">
            <img src="/images/city1.svg" alt="" />
          </li>
          <li class="ville" style="--left: 18; --scale: 5">
            <img src="/images/city2.svg" alt="" />
          </li>
          <li class="ville bird" style="--left: 16; --scale: 1; --top: 6">
            <img src="/images/bird.png" alt="" />
          </li>
                    <li class="ville human" style="--scale: .7;">
            <img src="/images/skate.png" alt="" />
          </li>
                              <li class="ville" style="--left: 23; --scale: 2">
            <img src="/images/house.png" alt="" />
          </li>
                              <li class="ville" style="--left: 19; --scale: 6">
            <img src="/images/city1.svg" alt="" />
          </li>
        </ul>
        <ul class="japan_village">
          <li class="ville" style="--left: 10; --scale: 3">
            <img src="/images/tako.png" alt="" />
          </li>
          <li class="ville" style="--left: 14; --scale: 2">
            <img src="/images/torii.png" alt="" />
          </li>
          <li class="ville" style="--left: 8; --scale: 1.3">
            <img src="/images/neko.png" alt="" />
          </li>
        </ul>
        <ul class="canada_village">
          <li class="ville" style="--left: 17; --scale: 4">
            <img src="/images/newyork.png" alt="" />
          </li>
          <li class="ville" style="--left: 11.8; --scale: 1.3">
            <img src="/images/racoon.png" alt="" />
          </li>
          <li class="ville" style="--left: 11; --scale: 1.3">
            <img src="/images/beaver.png" alt="" />
          </li>
                    <li class="ville" style="--left: 13; --scale: 1.3">
            <img src="/images/maple-syrup.png" alt="" />
          </li>
                    <li class="ville" style="--left: 14; --scale: 1.3">
            <img src="/images/maple-leaf.png" alt="" />
          </li>
        </ul>
        <ul class="night_village" :style="{ opacity: startNight ? 1 : 0 }">
          <li class="ville moon" style="--left: 10; --scale: 2; --top: 9">
            <img src="/images/moon.png" alt="" />
          </li>
                              <li class="ville" style="--left: 2; --scale: .3; --top: 11">
            <img src="/images/star.png" alt="" />
          </li>
                    <li class="ville" style="--left: 4; --scale: .5; --top: 7">
            <img src="/images/star.png" alt="" />
          </li>
                    <li class="ville star2" style="--left: 7; --scale: .6; --top: 10">
            <img src="/images/stars.png" alt="" />
          </li>
           <li class="ville star" style="--left: 8.5; --scale: .4; --top: 19">
            <img src="/images/stars.png" alt="" />
          </li>
        </ul>
      </div>
      <div class="bottom"></div>
    </div>

      <div class="gallary">
        <div id="japanGallary" ref="japanGallary">
          <Carousel :items="japanImages"></Carousel>
                  <span class="btn" @click="closeGallary"></span>
        </div>
        <div id="canadaGallary" ref="canadaGallary">
          <Carousel :items="canadaImages"></Carousel>
                  <span class="btn" @click="closeGallary"></span>
        </div>
      </div>

    <div class="sections" ref="horizonCon">
      <section id="heroSection">
        <!-- <h1 class="title">Milla's life story</h1> -->
      </section>
      <section id="aboutSection">
        <div class="text">
          <h3>자기소개</h3>
          <p>이름 : 최미나</p>
          <p>나이: 93년생 닭띠 게자리 황금돼지</p>
          <p>성남거주</p>
          <p>개발길드</p>
        </div>
      </section>
      <section id="about2Section">
        <div class="text">
          <p>이름 : 최미나</p>
          <p>나이: 30..</p>
          <p>직업: 개발자</p>
        </div>
      </section>
      <section id="japanSection">
        <div class="text">
          <h3>일본워킹홀리데이</h3>
          <p>오사카 거주</p>
          <p>유니클로 6개월(첫알바는 짤림)</p>
          <p>노래방을 자주갔다<button class="pic_btn" @click="showGallary('japan')">📸</button></p>
        </div>
      </section>
      <section id="canadaSection">
        <div class="text">
          <h3>캐나다 어학연수</h3>
          <p>왜갔는지 기억이안남</p>
          <p>놀고 먹고 놀고 먹고</p>
          <p>자주가던 술집이 있다<button class="pic_btn" @click="showGallary('canada')">📸</button></p>
        </div>
      </section>
      <section id="devSection">
        <div class="text">
          <h3>운칠기삼 합류 전</h3>
          <p>오래 일하고 싶어서 개발자가 됨</p>
          <p>개발은 많이 하였으나 리드를 못받았다</p>
          <p>회식을 좋아했다</p>
        </div>
      </section>
      <section id="workSection">
        <div class="text">
          <h3>운칠기삼 합류 후</h3>
          <p>스튜디오, 이벤트</p>
          <p>투데이탭</p>
          <p>자기개발이 많아졌다</p>
        </div>
      </section>
      <section id="work2Section">
        <div class="text">
          <h3>이것을 추구합니다</h3>
          <p>재밌게 일하기</p>
          <p>독창성을 장려하는 개발자</p>
          <p>발전,,</p>
        </div>
      </section>
      <section id="brandSection">
        <div class="text">
          <h3>당신이 좋아하는 브랜드는? 혹은 좋아하는 영화? 노래? 책은?</h3>
          <p>다이소</p>
          <p>영어공부를 위한 것들</p>
        </div>
      </section>
      <section id="finalSection"></section>
    </div>
  </div>
</template>

<script>
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { gsap } from "gsap";
import Carousel from "@/components/Carousel2.vue";

export default {
  components: {
    Carousel,
  },
  data() {
    return {
      canadaImages: [
        "/images/canada/canada1.JPG",
        "/images/canada/canada2.JPG",
        "/images/canada/canada3.JPG",
        "/images/canada/canada4.JPG",
        "/images/canada/canada5.JPG",
        "/images/canada/canada6.JPG",
        "/images/canada/canada7.JPG",
        "/images/canada/canada8.JPG",
        "/images/canada/canada9.JPG",
        "/images/canada/canada10.JPG",
        "/images/canada/canada11.JPG",
      ],
      japanImages: [
        "/images/japan/japan1.JPG",
        "/images/japan/japan2.JPG",
        "/images/japan/japan3.JPG",
        "/images/japan/japan4.JPG",
      ],
      showThirdIndex: 0,
      backgroundColor: "#96c6f1",
      startNight: false,
    };
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    this.setScroll();
    this.setHero();
    this.setAbout();
    this.setCanada();
    this.setJapan();
    this.setDev();
    this.setFinal();
  },
  methods: {
    setScroll() {
      let panelsContainer = this.$refs.horizonCon;

      const panels = gsap.utils.toArray("section");
      const tl = gsap.timeline({
        scrollTrigger: {
          trigger: "#home",
          pin: true,
          scrub: 2.5,
          end: () => "+=" + (panelsContainer.offsetWidth - innerWidth),
        },
      });
      tl.add("start").to(
        panels,
        {
          xPercent: -100 * (panels.length - 1),
          ease: "none",
        },
        "start"
      );
      tl.call(() => {
        gsap.to("#heroSection .title", { scale: 0, x: 2000, duration: 0.1 });
      }, "start");
      tl.to(".third_village", { x: -1300 }, "start");
      tl.to(".second_village", { x: -600 }, "start");
      tl.to(".first_village", { x: -200 }, "start");

      tl.to(".japan_village", { x: -1300 }, "start");
      tl.to(".canada_village", { x: -1300 }, "start");
      tl.to(".first_cloud", { x: -100 }, "start");
      tl.to(".second_cloud", { x: -130 }, "start");
    },
    setHero() {
      const tl = gsap.timeline({
        scrollTrigger: {
          trigger: "#heroSection",
          //toggleActions: "play reverse play reverse",
          scrub: 1,
          start: () => "top top",
          end: () => "+=" + document.querySelector("#heroSection").offsetWidth,
        },
      });
      tl.to(".title", { opacity: 0 });
    },
    setAbout() {
      const tl = gsap.timeline({
        toggleActions: "play reverse play reverse",
        scrollTrigger: {
          trigger: "#aboutSection",
          start: "center",
        },
      });
      tl.to(".bird", {
        keyframes: [
          { x: -400, y: 30 },
          { x: -800, y: 100 },
          { x: -1200, y: 0 },
          { x: -1600, y: 100 },
          { x: -3000, y: 180 },
        ],
        duration: 3,
      }, '+=1');
    },
    setJapan() {
      const tl = gsap.timeline({
        scrollTrigger: {
          trigger: "#japanSection",
          toggleActions: "play reverse play reverse",
          start: () =>
            "top top-=" +
            (document.querySelector("#japanSection").offsetLeft -
              window.innerWidth / 2),
          end: () => "+=" + document.querySelector("#japanSection").offsetWidth,
        },
      });
      tl.to(".japan_village", { opacity: 1, duration: 1 });
    },
    setCanada() {
      const tl = gsap.timeline({
        scrollTrigger: {
          trigger: "#canadaSection",
          toggleActions: "play reverse play reverse",

          onLeave: () => {
            this.backgroundColor = "#82688b";
          },
          onLeaveBack: () => {
            this.backgroundColor = "#96c6f1";
          },
          start: () =>
            "top top-=" +
            (document.querySelector("#canadaSection").offsetLeft -
              window.innerWidth / 2),
          end: () =>
            "+=" + document.querySelector("#canadaSection").offsetWidth,
        },
      });
      tl.add("start");
      tl.to(".canada_village", { opacity: 1, duration: 1 }, "start");
    },
    setDev() {
      const tl = gsap.timeline({
        scrollTrigger: {
          trigger: "#devSection",
          toggleActions: "play reverse play reverse",
          onEnter: () => {
            this.startNight = true;
            gsap.from('.moon', { rotate: 180 , duration: 1})
          },
          onLeave: () => {
            this.backgroundColor = "#484848";
          },
          onLeaveBack: () => {
            this.startNight = false;
          },
          onEnterBack: () => {
            this.backgroundColor = "#82688b";
          },
          start: () =>
            "top top-=" +
            (document.querySelector("#devSection").offsetLeft -
              window.innerWidth / 2),
          end: () => "+=" + document.querySelector("#devSection").offsetWidth,
        },
      });
    
    },
    setFinal() {
      const tl = gsap.timeline({
        scrollTrigger: {
          trigger: "#finalSection",
          toggleActions: "play reverse play reverse",
          start: () =>
            "top top-=" + document.querySelector("#finalSection").offsetLeft,
          end: () => "+=" + document.querySelector("#finalSection").offsetWidth,
        },
      });
      tl.to(".final_title", { opacity: 1, duration: 1 });
    },
    showGallary(type) {
      this.$refs[`${type}Gallary`].style.transform = 'scale(1)';
    },
    closeGallary() {
      this.$refs.canadaGallary.style.transform = 'scale(0)';
      this.$refs.japanGallary.style.transform = 'scale(0)';
    }
  },
};
</script>

<style lang="scss" scoped>
#home {
  height: 100vh;
  overflow: hidden;
}
.static {
  position: absolute;
  left: 0;
  top: 0;
  right: 0;
  bottom: 0;
  //z-index: 1000;
  .sky {
    height: calc(100vh - 200px);
    width: 100%;
    background: #96c6f1;
    transition: all 0.5s;
  }
  .bottom {
    height: 200px;
    width: 100%;
    background: #764e47;
    bottom: 0;
  }
  & > * {
    position: absolute;
  }
}

ul[class$="village"] {
  position: absolute;
  width: 100%;
  height: 100%;
  .ville {
    position: absolute;
    bottom: 0;
    left: calc(var(--left) * 130px);
    top: calc(var(--top) * 10px);
    width: calc(var(--scale) * 100px);
    img {
    }
  }
}
.japan_village {
  opacity: 0;
  z-index: 4;
  left: 10%;
}
.canada_village {
  opacity: 0;
  z-index: 4;
  left: 5%;
}
.first_village {
  opacity: 0.5;
  z-index: 1;
}
.night_village {
  transition: opacity 0.5s;
  opacity: 0;
  z-index: 1;
}
.second_village {
  opacity: 0.9;
  z-index: 2;
}
.third_village {
  z-index: 3;
}
.clouds {
  position: absolute;
  width: 100%;
  height: 100%;

  .cloud {
    position: absolute;
    top: 0;
    left: 0;
  }
}

.sections {
  //height: calc(100vh - 200px);
  height: 100%;
  min-width: 100vw;
  width: 1500vw;
  display: flex;
  z-index: 10;
}
section {
  width: 150vw;
  height: 100%;
  display: flex;
  position: relative;
  justify-content: center;
}
.text {
  background: #fef9ed;
  outline-color: #fef9ed;
  border-color: #5d5d5e;
  box-shadow: 0 15px 20px rgb(0 0 0 / 30%);
  min-width: 300px;
  opacity: 0.95;
  margin: 10px;
  border: 1px black solid;
  outline: 10px #fef9ed solid;
  color: black;
  padding: 30px;
  h3 {
    font-weight: 600;
    margin-bottom: 15px;
  }
  p {
    margin-bottom: 5px;
  }
}
.title,
.final_title {
  padding: 1.5em 0;
  width: 100%;
  font-size: 9em;
  color: #fff;
  font-weight: bold;
  text-align: center;
  z-index: 2;
}
.final_title {
  opacity: 0;
}
#heroSection {
}
section {
  z-index: 1;
  .text {
    font-size: 2em;
    position: absolute;
    left: 50%;
    top: 200px;
    transform: translateX(-50%);
  }
}
.images {
  .image {
    width: 300px;
  }
}
#canadaSection {
}
.pic_btn {
  border: none;
  font-size: 30px;
  cursor: pointer;
}
.gallary {
  position: fixed;
    top: 10%;
    right: 40%;
    z-index: 100;
  & > div {
    position: absolute;
    width: 500px;
    height: 650px;
    transform: scale(0);
    border: 30px solid #fff;
    border-top: 40px solid #fff;
    border-bottom: 40px solid #fff;
    border-radius: 15px;
        transition: transform 1s;
    .btn {
      position: absolute;
      left: 50%;
      width: 30px;
      height: 30px;
      border-radius: 100%;
      border: 4px outset #d5d5d5;
      bottom: -35px;
      transform: translateX(-50%);
    }
  }
}
.human {
  left: 165vw !important;
  z-index: 100;
  animation: skate 10s linear infinite;
}
.star {
  animation: 3s blink infinite;
}
.star2 {
  animation: 3s blink infinite;
  animation-delay: 1s;
}
@keyframes skate {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-170vw);
  }
}
@keyframes blink {
  0%, 100% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
}
</style>