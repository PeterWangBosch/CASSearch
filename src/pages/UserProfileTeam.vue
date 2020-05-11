<template>
    <div class="row">
      <div class="col-xl-4 col-lg-5 col-md-6">
        <user-card-team>

        </user-card-team>
        <members-card>

        </members-card>
      </div>
      <div class="col-xl-8 col-lg-7 col-md-6">
        <edit-profile-form>

        </edit-profile-form>
      </div>
    </div>
</template>
<script>
import EditProfileFormTeam from "./UserProfile/EditProfileFormTeam.vue";
import UserCardTeam from "./UserProfile/UserCardTeam.vue";
import MembersCard from "./UserProfile/MembersCard.vue";
export default {
  components: {
    EditProfileFormTeam,
    UserCardTeam,
    MembersCard
  }
};
</script>
<style>
</style>
