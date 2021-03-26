<template>
  <div :class="$style.box" id="scroll_t">
    <div :class="[$style.protocol, $style.border_protocol]">
      <div :class="$style.corona_image">
        <img src="@/assets/imgs/corona.png" />
      </div>
      <div :class="$style.protocolImage">
        <img src="@/assets/imgs/protocol.png" />
      </div>
      <h1>
        رعایت پروتکل ورود به مطب
      </h1>
      <div :class="$style.image_dash">
        <img src="@/assets/imgs/4-whit.png" />
      </div>
      <p>
        سلامتی شما برای ما شرط اول است، به همین منظور برای ورود به مطب تمام
        پروتکل های لازم اجرا میشود.
      </p>
    </div>
    <div :class="[$style.protocol, $style.bcp]">
      <div :class="$style.protocolImage">
        <img src="@/assets/imgs/natural.png" />
      </div>
      <h1>زیبایی طبیعی</h1>
      <div :class="$style.image_dash">
        <img src="@/assets/imgs/4-whit.png" />
      </div>
      <p>
        استفاده از جدیدترین متدهای جوانسازی و بهترین مواد اولیه جهت افزایش
        زیبایی طبیعی، هنر ماست.
      </p>
    </div>
    <div :class="$style.makeup">
      <img :class="$style.def_image" src="@/assets/imgs/makeup.png" />
    </div>
    <div :class="$style.protocol">
      <div :class="$style.protocolImage">
        <img src="@/assets/imgs/material.png" />
      </div>
      <h1>استفاده از مواد و متریال اصل و دارای تاییدیه</h1>
      <div :class="$style.image_dash">
        <img src="@/assets/imgs/4-whit.png" />
      </div>
      <p>
        استفاده از مواد اولیه اورجینال، بدون عوارض جانبی. کلیه مواد مورد
        استفاده، در حضور شما باز می شود و برای اطمینان بیش تر جعبه در اختیار شما
        قرار خواهد گرفت.
      </p>
    </div>
    <div :class="[$style.protocol, $style.bcp]">
      <div :class="$style.protocolImage">
        <img src="@/assets/imgs/doctor.png" />
      </div>
      <h1>تجربه و مهارت پزشک</h1>
      <div :class="$style.image_dash">
        <img src="@/assets/imgs/4-whit.png" />
      </div>
      <p>
        بیش از 10 سال سابقه در زمینه زیبایی و جوانسازی با استفاده ازبهترین و
        جدیدترین متدهای روز دنیا.
      </p>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'NotesMain'
  };
</script>

<style lang="scss" module>
  .box {
    padding-top: 35px;
    background: url('./../../assets/imgs/5.jpg');
    background-repeat: no-repeat;
    background-size: cover;
  }

  .protocol {
    background: #bb9ce4;
    padding-top: 1px;
    margin: 0 15px 30px;
    padding-bottom: 1px;
    border-radius: 20px;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
    &.border_protocol {
      border: 5px solid #d8c171;
    }
    &.bcp {
      background: #ffb89f;
    }
    h1 {
      color: #fff;
      font-size: 18px;
      font-weight: bold;
      text-align: center;
      line-height: 28px;
    }
    p {
      margin: 3px 11px 7px;
      font-size: 14px;
      color: #fff;
      text-align: justify;
      text-align-last: center;
    }
  }
  .corona_image {
    position: relative;
    width: 90px;
    margin: -13px 0px 0 37px;
    float: left;
    img {
      width: 100%;
    }
  }
  .protocolImage {
    position: relative;
    width: 80px;
    height: 80px;
    margin: 4px auto 7px;
    img {
      width: 100%;
      position: absolute;
    }
    /*  &::before {
        content: '';
        display: block;
        padding-bottom: 100%;
      }
     img {
        overflow: hidden;
        position: absolute;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        width: 100%;
      } */
  }
  .image_dash {
    margin: 6px 35.3% 3px;
    img {
      width: 100%;
      display: block;
    }
  }
  .makeup {
    position: relative;
    margin: -25px 18px 0px 18px;
    &::before {
      content: '';
      display: block;
      padding-bottom: 71.9%;
    }
    img {
      overflow: hidden;
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      width: 100%;
    }
  }
</style>
