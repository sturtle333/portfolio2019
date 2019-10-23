<template>
<div class="contents-container-about">
  <div style="align-self: stretch;">
    <p style="margin: 0; text-align: left; font-size: 3em;">About.</p>
    <hr style="border: 2px solid #54546c;">
  </div>
  <div style="display: flex; flex-direction: row; align-items: center; justify-content: center; flex: 1;">
    <div class="about-desc">
      <div>
        <div>
          <div class="about-emoji"><span>📑</span></div>
          <span class="about-info">PARK JUNGHO (박정호)</span>
        </div>
        <div>
          <div class="about-emoji"><span>🎂</span></div>
          <span class="about-info">December, 1st, 2001 (2001.12.01)</span>
        </div>
        <div>
          <div class="about-emoji"><span>📧</span></div>
          <span class="about-info">sturtle333@gmail.com</span>
        </div>
        <div>
          <div class="about-emoji"><span>📱</span></div>
          <span class="about-info">010-8780-0934</span>
        </div>
        <p>if you want view more private information, contact me</p>
      </div>
    </div>
    <div class="about-pic">
      <img class="selfy" src="../../assets/selfy.png" alt="myPicture" />
    </div>
  </div>
</div>
</template>

<script>
export default {
  name:'about'
}
</script>

<style>
.contents-container-about div {
  display: inline-block;
}
.contents-container-about span {
  display: inline-block;
}

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
.contents-container-about .about-desc {
  display: flex;
  flex-direction: column;
  align-items: center;
  flex: 1 0;
}
.contents-container-about .about-pic {
  display: flex;
  flex-direction: center;
  flex: 1 1;
  justify-content: flex-end;
}
.selfy {
  float: right;
  width: 70%;
  padding: 20px;
  background-color: white;
}


.contents-container-about .about-desc > div > div {
  display: flex;
  flex-directiom: row;
  align-items: center;
  align-self: flex-start;

  margin-bottom: 1em;
}

.contents-container-about .about-desc > div > div:hover {
  color: white;
  border-radius: 30px;
  background-color: #54546c;
}


.contents-container-about .about-desc * {
  display: inline-block;
  font-size: 1.2em;
}


.about-info {
  margin-left: 2em;
}


.about-emoji {
  text-align: center;
  vertical-align: middle;

  border-radius: 30px;
  padding: 10px;

  background-color: #54546c;
}
.about-emoji>span{
  width: 1.3em;
  text-align: center;
}
</style>
