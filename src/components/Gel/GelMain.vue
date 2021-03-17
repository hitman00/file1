<template>
  <div :class="$style.main">
    <div :class="$style.box">
      <Syringe>
        <img src="@/assets/imgs/Syringe.jpg" />
      </Syringe>
      <div :class="$style.textbox">
        <ul>
          <li>
            <Imageicon />
            <div :class="$style.qustion">از تزریق ژل می ترسید؟</div>
          </li>
          <li>
            <Imageicon />
            <div :class="$style.qustion">
              از غیر طبیعی شدن حالت صورتتان بعد از تزریق ژل می ترسید؟
            </div>
          </li>
          <li>
            <Imageicon />
            <div :class="$style.qustion">
              نگران جا به جایی ژل بعد از تزریق هستید؟
            </div>
          </li>
          <li>
            <Imageicon />

            <div :class="$style.qustion">
              نگران ایجاد کبودی بعد از تزریق ژل هستید؟
            </div>
          </li>
          <li>
            <Imageicon />

            <div :class="$style.qustion">
              دوست دارید بعد از انجام خدمات جوانسازی و تزریق ژل، همچنان زیبایی
              طبیعی چهره شما حفظ شود؟
            </div>
          </li>
        </ul>
      </div>
      <div :class="$style.title">
        تزریق <span>ژل جوانسازی </span> با متد انحصاری دکتر فرشته زمانی
      </div>

      <Underline>
        <img src="@/assets/imgs/underline.png" />
      </Underline>
      <div :class="$style.text">
        پوست با گذشت زمان دچار افتادگی و تحلیل چربی های زیر پوستی می شود . توصیه
        ما در ابتدا انجام کارهای جوانسازی پایه ای مثل هایفوتراپی و آراف فرکشنال
        می باشد. در صورت نیاز، در ادامه می توانیم با تزریق ژل، حجم از دست رفته
        بافت های زیر پوستی را جبران کنیم.<br />
        ما به شما اطمینان می دهیم که با استفاده از بهترین برندهای روز دنیا مثل
        ژل الانسه که خاصیت کلاژن سازی نیز دارد، تزریقی بسیار زیبا و متناسب با
        فرم طبیعی صورت خود خواهید داشت. شما همچنین می توانید با مطالعه نظرات و
        بازدید از صفحه اینستاگرام ما، از تجربیات و رضایتمندی سایر خدمات گیرندگان
        آگاه شوید.
      </div>

      <div :class="[$style.title, $style.fixtext2]">ژل الانسه ELLANSE</div>

      <Underline>
        <img src="@/assets/imgs/underline.png" />
      </Underline>
      <div :class="$style.text">
        ما در کلاب زیبایی و سلامتی دکتر فرشته زمانی، با توجه به نیاز شما از
        بهترین و معتبرترین انواع مواد اولیه در دنیا استفاده می کنیم. از بهترین
        برندهای ژل در دنیا، ژل الانسه است. مهم ترین مزیت این ژل نسبت به سایر
        محصولات مشابه را می توان خاصیت جوان سازی و کلاژن سازی همزمان با ایجاد
        فرم دهی و حجم دهی فوق العاده آن دانست. ژل الانسه، تنها برند ژل موجود در
        ایران است که با داشتن فرمولی استثنایی ماندگاری آن 2 سال تا 4 سال می
        باشد.
        <br />
        دکتر فرشته زمانی با شرکت در معتبرترین دوره های روز دنیا، از جدیدترین و
        متفاوت ترین روش ها جهت تزریق استفاده می کنند. بنابراین شما عزیزان می
        توانید از نتیجه طبیعی و فوق العاده تزریق، اطمینان کامل داشته باشید.
      </div>

      <div :class="$style.rollimage">
        <Images />
      </div>
    </div>
  </div>
</template>

<script>
  import Syringe from './Syringe.vue';
  import Imageicon from './ImageIcon';
  import Underline from './Underline.vue';
  import Images from './GelImages.vue';
  export default {
    name: 'GelMainl',
    components: {
      Syringe,
      Imageicon,
      Underline,
      Images
    }
  };
</script>

<style lang="scss" module>
  .main {
    width: 100%;
    float: left;

    .box {
      margin: 4px 10px 96px 10px;
      .textbox {
        width: 100%;
        padding: 0px 20px;
        position: relative;
        margin-top: -9px;
        ul li {
          padding-bottom: 21.5px;

          .qustion {
            overflow: hidden;
            color: #34394d;
            font-size: 12.5px;
            line-height: 1.8;
            word-spacing: -1.2px;
            padding: 1px 6px 0 6px;
          }
        }
      }
      .title {
        font-size: 15px;
        letter-spacing: -0.3px;
        word-spacing: -0.6px;
        margin-bottom: -10px;
        color: #030303;
        padding: 7px 24px 0 0;
        span {
          font-weight: 600;
          font-size: 15px;
          color: #000;
        }
      }
      .text {
        font-size: 14px;
        text-align: justify;
        color: #444243;
        word-spacing: -2.2px;
        letter-spacing: -0.2px;
        padding: 7px 24px 0 35px;
        line-height: 1.5;
      }
      .fixtext2 {
        padding-top: 28px;
      }
      .rollimage {
        margin-top: 29px;
      }
    }
  }
</style>
