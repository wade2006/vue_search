<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
    <router-view />
  </div>
</template>

<style>
body {
  margin: 0;
  color: rgba(0, 0, 0, 0.65);
  font-size: 14px;
  font-family: -apple-system, BlinkMacSystemFont, Segoe UI, PingFang SC,
    Hiragino Sans GB, Microsoft YaHei, Helvetica Neue, Helvetica, Arial,
    sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol;
  font-variant: tabular-nums;
  line-height: 1.5;
  background-color: #fff;
  font-feature-settings: "tnum";
}
@font-face {
  font-family: "iconfont"; /* project id 2282833 */
  src: url("//at.alicdn.com/t/font_2282833_xstjgdupcm.eot");
  src: url("//at.alicdn.com/t/font_2282833_xstjgdupcm.eot?#iefix")
      format("embedded-opentype"),
    url("//at.alicdn.com/t/font_2282833_xstjgdupcm.woff2") format("woff2"),
    url("//at.alicdn.com/t/font_2282833_xstjgdupcm.woff") format("woff"),
    url("//at.alicdn.com/t/font_2282833_xstjgdupcm.ttf") format("truetype"),
    url("//at.alicdn.com/t/font_2282833_xstjgdupcm.svg#iconfont") format("svg");
}
.iconfont {
  font-family: "iconfont";
  font-size: 16px;
  font-style: normal;
}
</style>
