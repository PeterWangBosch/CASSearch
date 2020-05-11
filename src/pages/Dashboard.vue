<template>
  <div>

    <!--Charts-->
    <card >
      <div class="row py-2">
        <div class="col-3 text-center">
          <button type="button" style="padding: 12px 10px" class="btn btn-round btn-outline-primary ti-panel" @click="goDash">&nbsp;深度</button>
          </button>
        </div>
        <div class="col-3 text-center">
          <button type="button" style="padding: 12px 10px" class="btn btn-round btn-outline-primary ti-crown" @click="goStats">&nbsp;院士</button>
          </button>
        </div>
        <div class="col-3 text-center">
          <button type="button" style="padding: 12px 10px" class="btn btn-round btn-outline-primary ti-user" @click="goTeams">&nbsp;人才</button>
          </button>
        </div>
        <div class="col-3 text-center">
          <button type="button" style="padding: 12px 10px" class="btn btn-round btn-outline-primary ti-view-list-alt" @click="goTables">&nbsp;专利</button>
          </button>
        </div>
      </div>
      <div class="row py-2">
        <div class="col-3 text-center">
          <button type="button" style="padding: 12px 10px" class="btn btn-round btn-outline-primary ti-text" @click="goGraphs">&nbsp;成果</button>
          </button>
        </div>
        <div class="col-3 text-center">
          <button type="button" style="padding: 12px 10px" class="btn btn-round btn-outline-primary ti-pencil-alt2" @click="goIcons">&nbsp;论文</button>
          </button>
        </div>
        <div class="col-3 text-center">
          <button type="button" style="padding: 12px 10px" class="btn btn-round btn-outline-primary ti-map" @click="goMaps">&nbsp;资源</button>
          </button>
        </div>
        <div class="col-3 text-center">
          <button type="button" style="padding: 12px 10px" class="btn btn-round btn-outline-primary ti-bell" @click="goNotis">&nbsp;项目</button>
          </button>
        </div>
      </div>
    </card>

    <!--Stats cards-->
    <div class="row">
      <div class="col-md-6 col-xl-3" v-for="stats in statsCards" :key="stats.title">
        <stats-card>
          <div class="icon-big text-center" :class="`icon-${stats.type}`" slot="header">
            <i :class="stats.icon"></i>
          </div>
          <div class="numbers" slot="content">
            <p>{{stats.title}}</p>
            {{stats.value}}
          </div>
          <div class="stats" slot="footer">
            <i :class="stats.footerIcon" v-if="stats.footerIcon"></i> {{stats.footerText}}
          </div>
        </stats-card>
      </div>
    </div>


  </div>
</template>
<script>
import { StatsCard, ChartCard } from "@/components/index";
import Chartist from 'chartist';
export default {
  components: {
    StatsCard,
    ChartCard
  },
  methods: {
    goDash: function () {
      console.log("aaa");
      this.$router.push({ path: "/dashboard" });
    },
    goStats: function () {
      console.log("aaa");
      this.$router.push({ path: "/stats" });
    },
    goTeams: function () {
      console.log("aaa");
      this.$router.push({ path: "/teams" });
    },
    goTables: function () {
      console.log("aaa");
      this.$router.push({ path: "/table-list" });
    },
    goGraphs: function () {
      console.log("aaa");
      this.$router.push({ path: "/typography" });
    },
    goIcons: function () {
      console.log("aaa");
      this.$router.push({ path: "/icons" });
    },
    goMaps: function () {
      console.log("aaa");
      this.$router.push({ path: "/maps" });
    },
    goNotis: function () {
      console.log("aaa");
      this.$router.push({ path: "/notifications" });
    },
  },
  /**
   * Chart data used to render stats, charts. Should be replaced with server data
   */
  data() {
    return {
      statsCards: [
        {
          type: "success",
          icon: "ti-server",
          title: "一种光胶晶体及激光芯片",
          value: "专利授权",
          footerText: "中科院福建物质结构研究所",
          footerIcon: ""
        },
        {
          type: "success",
          icon: "ti-wallet",
          title: "一种无机化合物晶体LuI3O8(IO3)2",
          value: "申请公开",
          footerText: "中科院福建物质结构研究所",
          footerIcon: ""
        },
        {
          type: "danger",
          icon: "ti-pulse",
          title: "新型绿色无醛粘合剂",
          value: "许可转让",
          footerText: "联系我们",
          footerIcon: "ti-mobile"
        },
        {
          type: "success",
          icon: "ti-star",
          title: "光催化CO2参与的芳基羧基化反应",
          value: "最新进展",
          footerText: "中科院福建物质结构研究所",
          footerIcon: ""
        }
      ],
    };
  }
};
</script>
<style>
</style>
