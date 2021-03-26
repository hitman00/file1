<template>
  <div :class="$style.main">
    <div :class="$style.box">
      <div :class="$style.syringe">
        <img src="@/assets/imgs/Syringe.jpg" />
      </div>
      <div :class="$style.textbox">
        <ul>
          <li v-for="(items, id) in textbox" :key="id">
            <div :class="$style.icon">
              <img src="@/assets/imgs/icon.png" />
            </div>
            <div :class="$style.qustion">{{ items.comment }}</div>
          </li>
        </ul>
      </div>
      <div :class="$style.answer_box" v-for="(i, ke) in abox" :key="ke">
        <div :class="$style.title">{{ i.title }}</div>
        <div :class="$style.underline">
          <img src="@/assets/imgs/underline.png" />
        </div>
        <div :class="$style.text" v-html="i.text"></div>
      </div>
      <div :class="$style.rollimage">
        <Images />
      </div>
    </div>
  </div>
</template>

<script>
  import Images from './GelImages.vue';
  export default {
    name: 'GelMain',
    data: () => ({
      textbox: [
        {comment: 'از تزریق ژل می ترسید؟'},
        {comment: ' از غیر طبیعی شدن حالت صورتتان بعد از تزریق ژل می ترسید؟ '},
        {comment: ' نگران جا به جایی ژل بعد از تزریق هستید؟ '},
        {comment: ' نگران ایجاد کبودی بعد از تزریق ژل هستید؟ '},
        {
          comment:
            ' دوست دارید بعد از انجام خدمات جوانسازی و تزریق ژل، همچنان زیبایی طبیعی چهره شما حفظ شود؟ '
        }
      ],
      abox: [
        {
          title: ' تزریق ژل جوانسازی با متد انحصاری دکتر فرشته زمانی ',
          text:
            ' پوست با گذشت زمان دچار افتادگی و تحلیل چربی های زیر پوستی می شود . توصیه ما در ابتدا انجام کارهای جوانسازی پایه ای مثل هایفوتراپی و آراف فرکشنال می باشد. در صورت نیاز، در ادامه می توانیم با تزریق ژل، حجم از دست رفته بافت های زیر پوستی را جبران کنیم. <br> ما به شما اطمینان می دهیم که با استفاده از بهترین برندهای روز دنیا مثل ژل الانسه که خاصیت کلاژن سازی نیز دارد، تزریقی بسیار زیبا و متناسب با فرم طبیعی صورت خود خواهید داشت. شما همچنین می توانید با مطالعه نظرات و بازدید از صفحه اینستاگرام ما، از تجربیات و رضایتمندی سایر خدمات گیرندگان آگاه شوید.'
        },
        {
          title: 'ژل الانسه ELLANSE',
          text:
            ' ما در کلاب زیبایی و سلامتی دکتر فرشته زمانی، با توجه به نیاز شما از بهترین و معتبرترین انواع مواد اولیه در دنیا استفاده می کنیم. از بهترین برندهای ژل در دنیا، ژل الانسه است. مهم ترین مزیت این ژل نسبت به سایر محصولات مشابه را می توان خاصیت جوان سازی و کلاژن سازی همزمان با ایجاد فرم دهی و حجم دهی فوق العاده آن دانست. ژل الانسه، تنها برند ژل موجود در ایران است که با داشتن فرمولی استثنایی ماندگاری آن 2 سال تا 4 سال می باشد. <br> دکتر فرشته زمانی با شرکت در معتبرترین دوره های روز دنیا، از جدیدترین و متفاوت ترین روش ها جهت تزریق استفاده می کنند. بنابراین شما عزیزان می توانید از نتیجه طبیعی و فوق العاده تزریق، اطمینان کامل داشته باشید.'
        }
      ]
    }),

    components: {
      Images
    }
  };
</script>

<style lang="scss" module>
  .main {
    width: 100%;
    float: left;

    .box {
      margin: -17px 10px 17px 10px;
      float: left;
      background: linear-gradient(
        0deg,
        rgba(255, 247, 245, 1) 0%,
        rgba(255, 255, 255, 1) 38%,
        rgba(255, 255, 255, 1) 100%
      );
    }
  }
  .syringe {
    position: relative;
    width: 100%;
    &:before {
      content: '';
      display: block;
      padding-bottom: 61%;
    }
    img {
      overflow: hidden;
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      box-shadow: -1px -4px 5px 0px rgba(172, 172, 172, 0.3);
      border-top-right-radius: 25px;
      border-top-left-radius: 25px;
      width: 100%;
    }
  }
  .textbox {
    width: 100%;
    padding: 0px 20px;
    position: relative;
    margin-top: -9px;
    ul li {
      padding-bottom: 21.5px;
      .icon {
        width: 23px;
        float: right;

        img {
          width: 100%;
          display: block;
        }
      }
    }
  }
  .qustion {
    overflow: hidden;
    color: #34394d;
    font-size: 12.5px;
    line-height: 1.8;
    word-spacing: -1.2px;
    padding: 1px 6px 0 6px;
  }

  .title {
    font-size: 15px;
    letter-spacing: -0.3px;
    word-spacing: -0.6px;
    margin-bottom: -10px;
    color: #030303;
    padding: 8px 24px 0 0;
  }
  .underline {
    position: relative;
    margin: 0 19px;
    &::before {
      content: '';
      display: block;
      padding-bottom: 11.5%;
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
  .text {
    font-size: 14px;
    text-align: justify;
    color: #444243;
    word-spacing: -2.2px;
    letter-spacing: -0.2px;
    padding: 6px 24px 21px 35px;
    line-height: 1.5;
  }

  .rollimage {
    margin-top: 9px;
  }
</style>
