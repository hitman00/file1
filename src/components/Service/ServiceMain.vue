<template>
  <div :class="$style.service">
    <div :class="$style.service_background">
      <div :class="$style.title">خدمات کلینیک</div>
      <div :class="$style.servic_image">
        <img src="@/assets/imgs/underlineService.png" alt="" />
      </div>
      <div :class="$style.listbox">
        <ListOfService
          v-for="(item, id) in listservice"
          :key="id"
          :services="item.name"
        />
      </div>
      <div :class="$style.listbox2">
        <ListOfService
          v-for="(iteams, id) in listservice2"
          :key="id"
          :services="iteams.lname"
        />
      </div>
    </div>
  </div>
</template>

<script>
  import ListOfService from './ListOfService.vue';
  export default {
    name: 'Service',
    data: () => ({
      listservice: [
        {
          name: 'درمان ریزش'
        },
        {
          name: 'تقویت مو'
        },
        {
          name: 'مزوتراپی مو'
        },
        {
          name: 'PRP'
        },
        {
          name: 'میکرونیدلینگ'
        },
        {
          name: 'مزوتراپی'
        },
        {
          name: 'لیزر'
        },
        {
          name: 'درمان منافذ پوستی'
        },
        {
          name: 'هایفوتراپی'
        },
        {
          name: 'تیکسل'
        }
      ],
      listservice2: [
        {
          lname: 'جوانسازی پوست با لیزر'
        },
        {
          lname: 'لیزر لک'
        },
        {
          lname: 'فیلر'
        },
        {
          lname: 'ژل'
        },
        {
          lname: 'مزو ژل'
        },
        {
          lname: 'بوتاکس'
        },
        {
          lname: 'درمان لک ، کک و مک'
        },
        {
          lname: 'رژیم کتوژنیک'
        },
        {
          lname: 'پلاژن تراپی'
        },
        {
          lname: 'آرف فرکشنال'
        }
      ]
    }),
    components: {
      ListOfService
    }
  };
</script>

<style lang="scss" module>
  .service {
    display: flex;
    width: 100%;
    .service_background {
      width: 100%;
      height: 409px;
      background: url('./../../assets/imgs/service.jpg');
      background-size: cover;
      background-repeat: no-repeat;
      margin: 0px 8px;
      padding: 0;
      .title {
        text-align: center;
        padding-top: 19px;
        color: #fff;
        font-weight: bold;
        font-size: 18px;
      }
      .servic_image {
        margin: 0px 94px;
        height: 39px;
        img {
          width: 100%;
          height: 100%;
        }
      }
      .listbox {
        float: right;
        width: 50%;
        padding: 15px 26px 0 0;
      }
      .listbox2 {
        float: right;
        width: 50%;
        padding: 15px 21px 0 0;
      }
    }
  }
</style>
