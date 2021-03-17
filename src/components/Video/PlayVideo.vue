<template>
  <div :class="$style.h_iframe_aparat_embed_frame">
    <span></span>
    <iframe
      src="https://www.aparat.com/video/video/embed/videohash/PnWir/vt/frame"
      title="معرفی کلاب سلامت و زیبایی دکتر فرشته زمانی"
      allowFullScreen="true"
      webkitallowfullscreen="true"
      mozallowfullscreen="true"
    >
    </iframe>
  </div>
</template>

<script>
  export default {
    name: 'Video'
  };
</script>

<style lang="scss" module>
  .h_iframe_aparat_embed_frame {
    position: relative;
    width: 100%;
    height: 302px;
  }
  .h_iframe_aparat_embed_frame .ratio {
    display: block;
    width: 100%;
    height: auto;
  }
  .h_iframe_aparat_embed_frame iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    span {
      display: block;
      padding-top: 57%;
    }
  }
</style>
