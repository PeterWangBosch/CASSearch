<template>
  <card class="card" title="科研综述">
    <div>
      <form @submit.prevent>

        <div class="row">
          <div class="col-md-12">
            <div class="form-group">
              <textarea rows="20" class="form-control border-input"
                        placeholder="Here can be your description"
                        v-model="user.aboutMe">

              </textarea>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-md-12">
            <div class="form-group">
              <textarea rows="5" class="form-control border-input"
                        placeholder="Here can be your description"
                        v-model="user.awards">

              </textarea>
            </div>
          </div>
        </div>
        <!--div class="text-center">
          <p-button type="info"
                    round
                    @click.native.prevent="updateProfile">
            Update Profile
          </p-button>
        </div-->
        <div class="clearfix"></div>
      </form>
    </div>
  </card>
</template>
<script>
export default {
  data() {
    return {
      user: {
        aboutMe: `    李小文院士致力于地物光学遥感和热红外遥感的基础研究和应用研究，他创建了Li-Strahler几何光学模型。
    李小文创建了植被二向性反射Li-Strahler几何光学模型，奠定了地物二向性反射研究中几何光学学派的基础。在对地定量遥感方面，力倡病态反演理论。在赫姆霍兹互易原理在地表遥感中适用性（尺度效应）研究方面，给出赫姆霍兹互易原理用于非均一像元二向性反射的约束条件。 [8] 
    李小文在普朗克定律在地表遥感中尺度效应研究方面，建立了适用于非同温地表热辐射方向性的概念模型，首创了普朗克定律用于非同温黑体平面的尺度修正式及一般的非同温三维结构非黑体表面热辐射在像元尺度上的方向性和波谱特征的概念模型。 [8] 
    李小文的遥感基础研究工作得到了中国国家自然科学基金委和中国国家科委的持续支持，并与中国以外的国家合作；据2018年7月北京师范大学地理学与遥感科学学院官网显示，李小文正在主持进行的研究项目及研究计划有：中国国家“九五”攀登预选项目 “地球表面能量交换的遥感定量研究”（1997～2000），中国国家863计划项目 “机载多角度、多光谱成像系统”（1998～2000），美国国家宇航局（NASA）项目 “热辐射方向性模型”（1998～2000），中国国家自然科学基金 “用热点卫星数据研究地表的热点效（49971059）”（2000～2002），中国国家重点基础研究发展规划（九七三）项目 “地球表面时空多变要素的定量遥感理论及应用”（2000-2005）。`,
        awards: `李小文先后主持国家自然科学基金重点项目，国家攀登项目，国家973项目等重大遥感基础研究项目，1994年获中国科学院自然科学一等奖，2000年获中国高校科学技术一等奖。`
      }
    };
  },
  methods: {
    updateProfile() {
      alert("Your data: " + JSON.stringify(this.user));
    }
  }
};
</script>
<style>
</style>
