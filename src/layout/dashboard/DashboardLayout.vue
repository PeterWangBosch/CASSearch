<template>
  <div class="wrapper">
    <side-bar>
      <template slot="links">
        <sidebar-link to="/dashboard" name="深度" icon="ti-panel"/>
        <sidebar-link to="/stats" name="院士" icon="ti-crown"/>
        <sidebar-link to="/teams" name="人才" icon="ti-user"/>
        <sidebar-link to="/table-list" name="专利" icon="ti-view-list-alt"/>
        <sidebar-link to="/typography" name="成果" icon="ti-text"/>
        <sidebar-link to="/icons" name="论文" icon="ti-pencil-alt2"/>
        <sidebar-link to="/maps" name="资源" icon="ti-map"/>
        <sidebar-link to="/notifications" name="项目" icon="ti-bell"/>
      </template>
      <mobile-menu>
        <li class="nav-item">
          <a class="nav-link">
            <i class="ti-panel"></i>
            <p>关于</p>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link">
            <i class="ti-settings"></i>
            <p>登录</p>
          </a>
        </li>
        <li class="divider"></li>
      </mobile-menu>
    </side-bar>
    <div class="main-panel">
      <top-navbar></top-navbar>

      <dashboard-content @click.native="toggleSidebar">

      </dashboard-content>

      <content-footer></content-footer>
    </div>
  </div>
</template>
<style lang="scss">
</style>
<script>
import TopNavbar from "./TopNavbar.vue";
import ContentFooter from "./ContentFooter.vue";
import DashboardContent from "./Content.vue";
import MobileMenu from "./MobileMenu";
export default {
  components: {
    TopNavbar,
    ContentFooter,
    DashboardContent,
    MobileMenu
  },
  methods: {
    toggleSidebar() {
      if (this.$sidebar.showSidebar) {
        this.$sidebar.displaySidebar(false);
      }
    }
  }
};
</script>
