<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
    <router-view/>
  </div>
</template>

<style>
body{
  margin: 0px;
  padding: 0px;
}
@font-face {
  font-family: 'iconfont';  /* project id 2282833 */
  src: url('//at.alicdn.com/t/font_2282833_iybi3vm4b68.eot');
  src: url('//at.alicdn.com/t/font_2282833_iybi3vm4b68.eot?#iefix') format('embedded-opentype'),
  url('//at.alicdn.com/t/font_2282833_iybi3vm4b68.woff2') format('woff2'),
  url('//at.alicdn.com/t/font_2282833_iybi3vm4b68.woff') format('woff'),
  url('//at.alicdn.com/t/font_2282833_iybi3vm4b68.ttf') format('truetype'),
  url('//at.alicdn.com/t/font_2282833_iybi3vm4b68.svg#iconfont') format('svg');
}
.iconfont{
  font-family: "iconfont";
  font-size: 16px;
  font-style: normal;
}
</style>
