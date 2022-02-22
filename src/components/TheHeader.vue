 <template>
  <header class="homePage">
    <div class="homePage__head">
      <div class="homePage__head-img">
        <img src="../assets/train.png" alt="поезд" />
      </div>
      <button @click="scrollDown">вниз</button>

      <div class="homePage__ellipse-container">
        <div class="homePage__ellipse thin"></div>
        <div class="homePage__ellipse yellow"></div>
      </div>
      <div class="homePage__bg"></div>
    </div>
    <div id="test">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum quia quasi consequuntur eum asperiores. Facere omnis iusto tempore explicabo sequi porro repellat molestias ut sapiente? Excepturi blanditiis voluptates nemo soluta?
      Expedita quidem eum impedit dolore adipisci aspernatur saepe temporibus architecto ipsum voluptate. Aspernatur cupiditate provident dignissimos, recusandae, dolor placeat officia minima vitae enim quibusdam tempora deserunt qui consequatur rerum dicta!
      Vel voluptatem veniam aliquam quibusdam, tenetur ut temporibus repellat, quisquam eaque nemo deserunt corporis quasi dolore unde dolores, quos quam ad tempore culpa accusamus amet? Maxime, repellendus. Nemo, velit dolorem?
      Blanditiis architecto exercitationem facilis, placeat excepturi earum incidunt quia molestiae distinctio molestias animi quos, aperiam similique vero laborum voluptas? Debitis rem expedita doloremque repellendus alias nobis blanditiis, odit obcaecati sed!
    </div>
  </header>
</template>
<script>
// import { TimeLineMax } from "gsap/all";
export default {
  name: "TheHeader",
  created() {
    // let tl = new TimelineMax();
    // tl.fromTo(".homePage__bg", 3, { opacity: 0 }, { opacity: 1 });
  },
  methods: {
    scrollDown() {
      const element = document.querySelector("#test");
      const top = element.offsetTop;
      window.scrollTo(0, top);
    },
  },
};
</script>

<style lang="scss">
.homePage {
  width: 100%;
  height: 100vh;
  &__head {
    width: 100%;
    height: 100vh;
  }
  &__bg {
    width: 100%;
    height: 100vh;
    background-image: url("https://media.istockphoto.com/photos/aerial-view-of-lake-tahoe-shoreline-with-mountains-and-turquoise-blue-picture-id1302742624");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  & button {
    position: absolute;
    left: 50%;
    bottom: 10%;
    z-index: 10;
  }
  &__head-img {
    width: 350px;
    height: 408px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -30%);
    z-index: 1;
    & img {
      max-width: 100%;
      width: 100%;
    }
  }
  &__ellipse-container {
    width: 408px;
    height: 408px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border-radius: 50%;
    margin: 0 auto;
    z-index: 2;
  }
  &__ellipse {
    position: absolute;
    top: 0;
    border-radius: 50%;
    border-style: solid;
  }
  &__ellipse.thin {
    width: 100%;
    height: 100%;
    border-width: 1px;
    border-color: #494949;
    opacity: 0.5;
  }
  &__ellipse.yellow {
    width: 90%;
    height: 90%;
    border-width: 10px;
    border-color: #FFEB00 transparent;
    transform: rotate(-45deg);
    top: 12px;
    left: 12px;
    animation: ellipseRotate 6s ease-in-out infinite;
  }
}

@keyframes ellipseRotate {
  0% {
    transform: rotate(-45deg);
  }
  100% {
    transform: rotate(-405deg);
  }
}
</style>