<template>
  <div class="payment">
    <div class="payment__video-wrapper">
      <video width="auto" height="100%" class="payment__video" playsinline autoplay muted loop>
        <source src="/assets/video/animation1.mp4" />
      </video>
    </div>
    <div class="payment__info">
      <div class="payment__info__title">
        Instant payments <br />
        From account to account <br />
        No hassle!
      </div>
      <div class="payment__info__text">Accept payments from anywhere in the world with just one click.</div>
      <div>
        <Button class="payment__button" />
      </div>
    </div>
  </div>
</template>

<script setup>
import Button from "../UI/Button.vue";
</script>

<style scoped>
.payment {
  position: relative;
  max-width: 100%;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  gap: 40px;
}

.payment__video-wrapper {
  position: relative;
  max-width: 100%;
  height: 544px;
  overflow: hidden;
  border-radius: 24px;
}

.payment__video {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  border-radius: 24px;
}

.payment__info__title {
  font-size: calc(18.70313px + 2.47917vw);
  letter-spacing: -1px;
  margin-bottom: 24px;
  font-weight: 600;
  line-height: 120%;
  margin-bottom: 24px;
  text-align: center;
}

.payment__info__text {
  font-size: calc(16px + (4 + 4 * 0.7) * (100vw - 375px) / 1920);
  font-weight: 400;
  margin-bottom: 40px;
  text-align: center;
}

.payment__button {
  color: #ffffff;
  width: 160px;
  background-color: rgb(13, 114, 255);
  padding: 16px 56px;
  transition: all 0.1s ease-in-out;
  line-height: 29.05px;
  justify-self: center;
}

.payment__info {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
