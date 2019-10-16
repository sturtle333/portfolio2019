<template>
  <div id="app">
    <main-page />
  </div>
</template>

<script>
import MainPage from "./components/mainPage.vue"

export default {
  name: 'App',
  data () {
    return {
      browserCaution: {
        korean: '본 사이트는 구글 크롬 브라우저에 최적화 되어 있습니다.'
      }
    }
  },
  components: {
    'main-page': MainPage
  },
  methods: {
    setCookie: function(cookie_name,value){
      var exdate = new Date();
      exdate.setDate(exdate.getDate() + 1);
      var cookie_value = escape(value) + '; expires=' + exdate.toUTCString();
      document.cookie = cookie_name + '=' + cookie_value;
    },
    getCookie: function(cookie_name) {
      var x, y;
      var val = document.cookie.split(';');
      for (var i = 0; i < val.length; i++) {
        x = val[i].substr(0, val[i].indexOf('='));
        y = val[i].substr(val[i].indexOf('=') + 1);
        x = x.replace(/^\s+|\s+$/g, '');
        if (x == cookie_name) {
          return unescape(y);
        }
      }
    }
  },
  mounted() {
    var agt = navigator.userAgent.toLowerCase();
    this.setCookie('browerCaution',true);
    if(this.getCookie('browerCaution') !== 'true'){
      if (agt.indexOf("msie") != -1) {
        var rv = -1;
        if (navigator.appName == 'Microsoft Internet Explorer') {
          alert('본 사이트는 구글 크롬 브라우저에 최적화 되어 있습니다.');
        }
      }
      else if (navigator.userAgent.indexOf('MSIE') !== -1 || navigator.appVersion.indexOf('Trident/') > 0) {
        alert('본 사이트는 구글 크롬 브라우저에 최적화 되어 있습니다.');
      }
    }
  }
}
</script>

<style>
html, body{
  width: 100%;
  height: 100%;
  margin: 0;
}
#app {
  width: inherit;
  height: inherit;
  margin: 0;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
button:focus {
  outline: none;
}
</style>
