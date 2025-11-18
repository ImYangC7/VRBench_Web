<script>
export default {
  data() {
    return {
      row1Images: [
        '/front/1.png',
        '/front/2.png',
        '/front/3.png',
        '/front/4.png',
        '/front/5.png',
        '/front/6.png',
        '/front/7.png',
        '/front/8.png',
        '/front/9.png',
        '/front/10.png',
      ],
      row2Images: [
        '/front/11.png',
        '/front/12.png',
        '/front/13.png',
        '/front/14.png',
        '/front/15.png',
        '/front/16.png',
        '/front/17.png',
        '/front/18.png',
        '/front/19.png',
        '/front/20.png',
      ],
    }
  },
}
</script>

<template>
  <div class="carousel-wrapper">
    <el-row justify="center">
      <el-col :span="24">
        <div class="carousel-row row-1">
          <div class="carousel-track track-left">
            <el-image
              v-for="path in row1Images"
              :key="`r1-${path}`"
              :src="path"
              fit="contain"
              class="carousel-image"
            />
            <!-- duplicate for seamless effect -->
            <el-image
              v-for="path in row1Images"
              :key="`r1b-${path}`"
              :src="path"
              fit="contain"
              class="carousel-image"
            />
          </div>
        </div>
      </el-col>
    </el-row>

    <el-row justify="center">
      <el-col :span="24">
        <div class="carousel-row row-2">
          <div class="carousel-track track-right">
            <el-image
              v-for="path in row2Images"
              :key="`r2-${path}`"
              :src="path"
              fit="contain"
              class="carousel-image"
            />
            <!-- duplicate for seamless effect -->
            <el-image
              v-for="path in row2Images"
              :key="`r2b-${path}`"
              :src="path"
              fit="contain"
              class="carousel-image"
            />
          </div>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<style scoped>
.carousel-wrapper {
  margin-top: 10px;
}

.carousel-row {
  overflow: hidden;
  white-space: nowrap;
  margin: 10px 0;
}

.carousel-track {
  display: inline-flex;
}

.carousel-image {
  width: 200px;
  height: 200px;
  margin: 0 8px;
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);
}

.track-left {
  animation: scroll-left 35s linear infinite;
}

.track-right {
  animation: scroll-right 35s linear infinite;
}

@keyframes scroll-left {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}

@keyframes scroll-right {
  0% {
    transform: translateX(-50%);
  }
  100% {
    transform: translateX(0);
  }
}
</style>
