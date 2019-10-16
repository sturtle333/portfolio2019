<template>
<div id="container">
  <div class="container-nav">
    <main-nav :pg="page" @setPage="uploadPage"></main-nav>
  </div>
  <div class="container-contents">
    <main-contents-welcome class="pages" :class="[{ 'component-actived': page===0 },{'component-not-actived': page!==0}]" />
    <main-contents-information class="pages" :class="[{ 'component-actived': page===1 },{'component-not-actived': page!==1}]" />
  </div>
</div>
</template>

<script>
import Navigation from './interface/nav.vue'
import Welcome from './contents/welcome.vue'
import Information from './contents/information.vue'

export default {
  name: 'mainPage',
  data () {
    return {
      page: 0
    }
  },
  methods: {
    uploadPage: function(pg){
      this.page = pg;
    }
  },
  components: {
    'main-nav': Navigation,
    'main-contents-welcome': Welcome,
    'main-contents-information': Information
  }
}
</script>

<style>
#container {
  width: inherit;
  height: inherit;
  display: flex;
  flex-direction: row;
  overflow: hidden;
}
#container .container-contents{
  display: flex;
  flex-direction: column;
  flex: 1;
  height: inherit;
}

.pages {
  position: inline;
}

.component-not-actived {
  transition: opacity 1s, visibility 0s 1s, height 0s 1s, flex 0s 1s, padding 0s 1s, align-self 0s 1s;
  visibility:hidden;
  opacity: 0;
  flex: initial;
  height: 0px;
  overflow: hidden;
  pointer-events: none;
}
.component-actived {
  transition: opacity 1s 1s, visibility 0s 1s, flex 0s 1s, padding 0s 1s;
  visibility:visible;
  align-self: stretch;
  opacity: 1;
  padding: 5%;
}
</style>
