<template>
  <div class="page h-full m-5">
    <div class="container-fluid">
      <div class="row">
        <div class="col d-flex justify-content-center align-items-center">
          <div class="card-section">
            <div class="card border-0" style="width: 24rem;">
              <div class="card-title-section position-relative m-3 text-center">
                <h5 class="card-title fw-bold">{{ pageName }}</h5>
                <span class="title-underline"></span>
              </div>
              <img :src="require('../assets/' + imageName + '.jpeg')" /> class="card-img-top img-fluid" alt="picture" />
              <div class="card-body">
                <div class="title-section bg-light text-secondary">{{ featureName }}</div>
                <ul class="m-3">
                  <li
                    class="text-start"
                    v-for="(item, index) in featuresArray"
                    :key="index"
                  >{{ item }}</li>
                  <!-- <li class="text-start">負責點燃引擎汽缸內之壓縮混合氣體，以提供行駛動力。</li> -->
                  <!-- <li class="text-start">負責點燃引擎汽缸內之壓縮混合氣體，以提供行駛動力。</li> -->
                  <li
                    class="text-start fs-3 big-item"
                    v-for="(item, index) in featuresBigArray"
                    :key="index"
                  >{{ item }}</li>
                </ul>
                <div class="title-section bg-light text-secondary">{{ replaceName }}</div>
                <ul class="m-3">
                  <li
                    class="text-start"
                    v-for="(item, index) in replaceArray"
                    :key="index"
                  >{{ item }}</li>
                </ul>
              </div>
              <!-- <ul class="list-group list-group-flush">
                <li class="list-group-item border-0">An item</li>
                <li class="list-group-item border-0">A second item</li>
                <li class="list-group-item border-0">A third item</li>
              </ul>-->
              <!-- <div class="card-body">
                <a href="#" class="card-link">Card link</a>
                <a href="#" class="card-link">Another link</a>
              </div>-->
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.page {
}
.card-title-section {
  .title-underline {
    &::before {
      content: "";
      position: absolute;
      left: 50;
      transform: translate(-50%);
      width: 30px;
      height: 2px;
      background-color: #000;
    }
  }
}
ul {
  li.big-item {
    list-style-image: url("../assets/star-fill.svg");
  }
}
</style>
<script>

export default {
  data() {
    return {
      pageName: "火星塞",
      featureName: "特色",
      featuresArray: [
        "負責點燃引擎汽缸內之壓縮混合氣體，以提供行駛動力。",
        "負責點燃引擎汽缸內之壓縮混合氣體，以提供行駛動力。",
        "負責點燃引擎汽缸內之壓縮混合氣體，以提供行駛動力。"
      ],
      featuresBigArray: [
        "建議定期更換，以確保引擎運轉效率和油耗表現。"
      ],
      replaceName: "更換/檢查週期",
      replaceArray: [
        "長效型：每十萬公里"
      ],
      imageName: "blueCar"

    }
  },
  name: 'Home',
  components: {
  }
}
</script>
