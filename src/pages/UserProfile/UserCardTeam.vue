# 1 "UserCard.vue"
# 1 "<built-in>"
# 1 "<command-line>"
# 31 "<command-line>"
# 1 "/usr/include/stdc-predef.h" 1 3 4
# 32 "<command-line>" 2
# 1 "UserCard.vue"
<template>
  <card class="card-user">
    <div slot="image">
      <img src="@/assets/img/background.jpg" alt="...">
    </div>
    <div>
      <div class="author">
        <img class="avatar border-white" src="@/assets/img/faces/lixiaowen.jpg" alt="...">
        <h4 class="title">李小文
          <br>
          <!--a href="#">
            <small>@chetfaker</small>
          </a-->
        </h4>
      </div>
      <p class="description text-center">
        中国遥感领域泰斗级专家
        <br> 中国科学院院士
      </p>
    </div>
    <hr>
    <!--div class="text-center">
      <div class="row">
        <div v-for="(info, index) in details" :key="index" :class="getClasses(index)">
          <h5>{{info.title}}
            <br>
            <span style="font-size:8px">{{info.subTitle}}</span>
          </h5>
        </div>
      </div>
    </div-->
  </card>
</template>
<script>
export default {
  data() {
    return {
      details: [
        {
          title: "",
          subTitle: "光学遥感"
        },
        {
          title: "",
          subTitle: "热红外遥感"
        },
        {
          title: "",
          subTitle: "非同温黑体平面"
        }
      ]
    };
  },
  methods: {
    getClasses(index) {
      var remainder = index % 3;
      if (remainder === 0) {
        return "col-lg-3 offset-lg-1";
      } else if (remainder === 2) {
        return "col-lg-4";
      } else {
        return "col-lg-3";
      }
    }
  }
};
</script>
<style>
</style>
