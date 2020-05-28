<template>
  <ListItem class="list-item-ewminfo">
    <img class="ewmimage" :src="ewmimage" alt srcset />
    <!-- <EditImage :src="image" class="img" height="18" width="18" /> -->
    <div class="ewminfotitle" contenteditable="true">{{ title }}</div>
  </ListItem>
</template>
<script>
import ListItem from "@/components/list-item";
import EditImage from "@/components/edit-image";
export default {
  name: "ListItemEwm",
  components: {
    ListItem,
    EditImage
  },
  props: {
    image: {
      type: String,
      default: require("@/assets/social-github.png")
    },
    ewmimage: {
      type: String,
      default: require("@/assets/ewm-miniapp.jpg")
    },
    title: {
      type: String,
      default: "github.com/luosijie"
    }
  }
};
</script>
<style lang="less">
.ewminfotitle {
  text-align: center;
  padding: 0px 0;
}
.ewmimage {
  width: 35%;
  margin: 0 auto;
  text-align: center;
}
.list-item-ewminfo {
  text-align: center;
  display: block;
  line-height: 5px;
  padding: 5px 0;
  .img {
    margin: 0 20px 0 15px;
  }

  span {
    font-size: 12px;
    color: #555;
  }
}
</style>
