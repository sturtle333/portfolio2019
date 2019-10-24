<template>
<div class="contents-container-about">
  <div style="align-self: stretch;">
    <p style="margin: 0; text-align: left; font-size: 3em;">About.</p>
    <hr style="border: 2px solid #54546c;">
  </div>
  <div class="about-content">
    <div class="about-desc">
      <p style="justify-self: flex-start; font-size: 3em;">
        potentiality
      </p>

      <item-info>
        <template #icon>📑</template>
        <template #desc>PARK JUNGHO (박정호)</template>
      </item-info>

      <item-info>
        <template #icon> 🎂</template>
        <template #desc> December, 1st, 2001</template>
      </item-info>

      <item-info>
        <template #icon> 📧</template>
        <template #desc>sturtle333@gmail.com</template>
      </item-info>

      <item-info>
        <template #icon> 📱</template>
        <template #desc>010-8780-0934</template>
      </item-info>
    </div>
    <img class="about-selfy" src="../../assets/selfy.png" alt="myPicture" />
  </div>
</div>
</template>

<script>
import INFO from './about/info.vue'

export default {
  name:'about',
  components: {
    'item-info': INFO
  }
}
</script>

<style>
.contents-container-about {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #ececf9;

  font-size: 14px;
  font-family: 'Inconsolate', sans-serif;
  color: #54546c;

  overflow: hidden;
}

.about-content {
  display: flex;
  flex: 1;
  align-self: stretch;

  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}
.about-desc {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: space-around;
  align-self: stretch;
}
.about-selfy {
  width: 40%;
  padding: 20px;
  background-color: white;
}


.about-info {
  margin-left: 1.5em;
  padding-right: 1.5em;
}
</style>
