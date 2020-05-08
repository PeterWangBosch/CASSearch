<template>
  <nav class="navbar navbar-expand-lg navbar-light">
    <div class="container-fluid">
      <div class="logo-title">
        <img src="@/assets/img/favicon.png" alt="" />
        <span></span>
      </div>
      <!--a class="navbar-brand" href="#">{{routeName}}</a-->
        <div style="margin-bottom: 0px;" class="input-group col-6">
            <input class="form-control border-right-0 border" type="search" value="团队 技术 项目">
            <span class="input-group-append">
                <div class="input-group-text bg-transparent"><i class="fa fa-search"></i></div>
            </span>
        </div>
      <button class="navbar-toggler navbar-burger"
              type="button"
              @click="toggleSidebar"
              :aria-expanded="$sidebar.showSidebar"
              aria-label="Toggle navigation">
        <span class="navbar-toggler-bar"></span>
        <span class="navbar-toggler-bar"></span>
        <span class="navbar-toggler-bar"></span>
      </button>
      <div class="collapse navbar-collapse">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item">
            <a href="#" class="nav-link">
              <i class="ti-panel"></i>
              <p>关于</p>
            </a>
          </li>
          <!--drop-down class="nav-item"
                     title="5 Notifications"
                     title-classes="nav-link"
                     icon="ti-bell">
            <a class="dropdown-item" href="#">Notification 1</a>
            <a class="dropdown-item" href="#">Notification 2</a>
            <a class="dropdown-item" href="#">Notification 3</a>
            <a class="dropdown-item" href="#">Notification 4</a>
            <a class="dropdown-item" href="#">Another notification</a>
          </drop-down-->
          <li class="nav-item">
            <a href="#" class="nav-link">
              <i class="ti-settings"></i>
              <p>
                登录
              </p>
            </a>
          </li>
        </ul>
      </div>
    </div></nav>
</template>
<script>
export default {
  computed: {
    routeName() {
      const { name } = this.$route;
      return this.capitalizeFirstLetter(name);
    }
  },
  data() {
    return {
      activeNotifications: false
    };
  },
  methods: {
    capitalizeFirstLetter(string) {
      return string.charAt(0).toUpperCase() + string.slice(1);
    },
    toggleNotificationDropDown() {
      this.activeNotifications = !this.activeNotifications;
    },
    closeDropDown() {
      this.activeNotifications = false;
    },
    toggleSidebar() {
      this.$sidebar.displaySidebar(!this.$sidebar.showSidebar);
    },
    hideSidebar() {
      this.$sidebar.displaySidebar(false);
    }
  }
};
</script>
<style lang="scss" scoped>
.logo-title {
  display: flex;
  align-items: center;
  padding-left: 5px;
  img {
    width: 34px;
    height: 34px;
  }

  span {
    font-size: 18px;
    font-family: "BoschSans-Bold";
    padding-left: 10px;
  }
}
</style>
