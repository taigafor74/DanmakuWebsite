<template>
  <div class="user-page-container">
    <UserHeader :userInfo="userInfo" />
    <UserMenu :userInfo="userInfo" />
    <div class="user-page-mt"><RouterView></RouterView></div>
    <!-- <DataView></DataView> -->
  </div>
</template>

<script setup lang="ts">
import UserHeader from "@/components/UserPage/UserHeader.vue";
import UserMenu from "@/components/UserPage/UserMenu.vue";
import DataView from "@/components/UserManage/DataView.vue";
import { getUserInfo } from "@/api/user";
import { useRoute } from "vue-router";
import { ref, onMounted, watch } from "vue";

const route = useRoute();
const userInfo = ref({});
const fetchUserInfo = async () => {
  const data = await getUserInfo(route.params.id);
  userInfo.value = data;
};

watch(
  () => route.params.id,
  async () => {
    await fetchUserInfo();
  }
);

onMounted(async () => {
  await fetchUserInfo();
});
</script>

<style lang="scss" scoped>
.user-page-container {
  margin: 0 auto;
  width: 75.161101vw;
  background-color: rgb(18, 18, 18);
  .user-page-mt {
    margin-top: 1vw;
  }
}
</style>
