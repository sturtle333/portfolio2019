<template>
<div class="info" @mouseover="isHover = true;" @mouseout="isHover = false">
  <div class="emoji" :class="{hovering: isHover}">
    <slot name="icon"></slot>
  </div>
  <div class="text" :class="{texthovering: isHover}">
    <slot name="desc"></slot>
  </div>
</div>
</template>

<script>
export default {
  name: 'info',
  data () {
    return {
      isHover: false
    }
  }
}
</script>

<style scoped>
.info {
  display: flex;
  flex-directiom: row;
  align-items: center;

  font-size: 20px;
  width: 20em;
  margin-bottom: 1em;
  border-radius: 30px;

  transition: color 1s;
  -webkit-transition: color 1s;
}
.info:focus {
  color: white;
  background-color: #54546c;
  font-weight: bold;

  padding-right: 1.4em;
}

.emoji {
  width: 1.4em;
  height: 1.4em;

  vertical-align: middle;

  border-radius: 30px;
  padding: 10px;

  background-color: #54546c;

  transition: width 0.5s;
}

.hovering {
  color: white;
  width: 100%;

  padding-right: 1.4em;
}

.text {
  transition: color 1s;

  position: absolute;
  margin-left: 3em;
  font-size: 1.2em;
}

.texthovering {
  color: white;
  font-weight: bold;
}
</style>
