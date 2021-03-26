<template>
  <div :class="$style.addresbar">
    <div :class="$style.box">
      <ul>
        <li v-for="(item, id) in detals" :key="id">
          <div :class="$style.image">
            <img src="@/assets/imgs/addresslogo.png" />
          </div>
          <h1>{{ item.title }}</h1>
          <p v-html="item.comment"></p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'AddressMain',
    data: () => ({
      detals: [
        {
          title: 'آدرس:',
          comment:
            'تهران، شهرک غرب، ایران زمین، خ مهستان، خ دوازدهم، پلاک ۲، درب پشت ساختمان، مطب دکتر فرشته زمانی '
        },
        {
          title: 'تلفن کلینیک:',
          comment: '۰۲۱ - ۸۸۳۶۷۶۴۴ <br/> ۰۲۱ - ۸۸۳۶۹۵۰۳'
        },
        {
          title: 'تلفن رزرو:',
          comment: '۰۹۰۱ - ۳۷۳۷۹۱۰ '
        }
      ]
    })
  };
</script>

<style lang="scss" module>
  .addresbar {
    width: 100%;
    display: flex;
    padding-bottom: 28px;
  }
  .box {
    margin: 0 8px;
    ul li {
      width: 100%;
      float: right;
      margin: 27px 0 -13px 0;
      .image {
        width: 25px;
        height: 26.5px;
        float: right;
        margin-left: 10px;
        margin-right: 20px;
        img {
          width: 100%;
          height: 100%;
        }
      }
      h1 {
        font-weight: 600;
        font-size: 17px;
        color: #000;
        line-height: 1.6;
      }
      p {
        margin: 4px 55px 5px 0;
        line-height: 1.5;
        font-size: 15px;
        direction: ltr;
      }
    }
  }
</style>
