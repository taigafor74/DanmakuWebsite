<template>
  <div class="item-con">
    <div class="left">
      <img :src="baseUrl + props.item?.img" />
    </div>
    <div class="right">
      <div class="a">
        <div class="title">
          {{ props.item?.title }}
        </div>
        <div style="margin-top: 5px">
          <span :class="statusClass">{{ status }}</span>
        </div>
        <div class="time">
          {{ new Date(props.item?.upload_date).toLocaleString() }}
        </div>
        <div class="bottom">
          <div class="icon">
            <img src="@/assets/icon/view.svg" />
            <span>{{ props.item?.playcount }}</span>
          </div>
          <div class="icon">
            <img src="@/assets/icon/dm.svg" />
            <span>{{ props.item?.danmacount }}</span>
          </div>
          <div class="icon">
            <img src="@/assets/icon/dz.svg" />
            <span>{{ props.item?.likecount }}</span>
          </div>
          <div class="icon">
            <img src="@/assets/icon/sc.svg" />
            <span>{{ props.item?.collectcount }}</span>
          </div>
          <div class="icon">
            <img src="@/assets/icon/fs.svg" />
            <span>{{ props.item?.sharecount }}</span>
          </div>
        </div>
      </div>
      <div class="btn">
        <el-button @click="edit">编辑</el-button>
        <el-button @click="dataview">数据</el-button>
      </div>
    </div>
  </div>
  <el-dialog v-model="showDialog" destroy-on-close>
    <UploadForm />
  </el-dialog>
  <el-dialog v-model="showData" destroy-on-close>
    <VideoDataView />
  </el-dialog>
</template>

<script setup lang="ts">
import { ref, onMounted, defineProps, watchEffect, computed } from "vue";
import UploadForm from "./UploadForm.vue";
import VideoDataView from "./VideoDataView.vue";
import { useUploadStore } from "@/stores/upload";
import { getTotalVideoComment } from "@/api/comment";
import { useVideoChartStore } from "@/stores/videochart";
const videochart = useVideoChartStore();
const store = useUploadStore();
const baseUrl = "http://localhost:3000/videoImg/";
const status = ref("(待审核)");
const props = defineProps({
  item: {
    type: Object,
    required: true,
  },
});
const showDialog = ref(false);
const showData = ref(false);
const edit = () => {
  store.resetAll();
  store.isEdit = true;
  showDialog.value = true;
  store.editForm = props.item;
  //   store.editForm.img = `http://localhost:3000/videoImg/${props.item.img}`;
};
const dataview = async () => {
  videochart.resetAll();
  const commentTotal = await getTotalVideoComment(props.item.vid);
  showData.value = true;
  videochart.vid = props.item.vid;
  videochart.form = props.item;
  videochart.item = [
    { name: "新增点赞", index: 1, num: 0, origin: props.item.likecount },
    { name: "新增评论", index: 2, num: 0, origin: commentTotal },
    { name: "新增播放", index: 3, num: 0, origin: props.item.playcount },
    { name: "新增收藏", index: 4, num: 0, origin: props.item.collectcount },
    { name: "新增弹幕", index: 5, num: 0, origin: props.item.danmacount },
  ];
  //   console.log(commentTotal);
};
watchEffect(() => {
  if (props.item) {
    if (props.item.status === "approved") {
      status.value = "(已通过)";
    } else if (props.item.status === "rejected") {
      status.value = "(未通过)";
    } else {
      status.value = "(待审核)";
    }
  }
});
const statusClass = computed(() => {
  if (props.item) {
    if (props.item.status === "approved") {
      return "status-approved";
    } else if (props.item.status === "rejected") {
      return "status-rejected";
    } else {
      return "status-pending";
    }
  }
});
</script>

<style lang="scss" scoped>
.status-approved {
  color: green;
}
.status-rejected {
  color: red;
}
.status-pending {
  color: yellow;
}

.item-con {
  padding: 24px 0;
  display: flex;
  .left {
    width: 154px;
    margin-right: 24px;
    height: 96px;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
  .right {
    flex: 1;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .a {
      .title {
      }
      .time {
        padding: 10px 0 20px 0;
        font-size: 14px;
        color: #8b8a8a;
        line-height: 16px;
        margin-right: 4px;
      }
      .bottom {
        display: flex;
        .icon {
          img {
            width: 15px;
            height: 15px;
          }
          display: flex;
          -webkit-box-align: center;
          align-items: center;
          margin-right: 25px;
          span {
            margin-left: 5px;
            font-size: 12px;
          }
        }
      }
    }
    .btn {
      display: flex;
      align-items: center;
    }
  }
}
</style>
