<template>
  <div>
    <div class="weui_cells_title" v-if="title" :style="{color:titleColor}" v-html="title"></div>
    <div class="weui_cells" :class="{'vux-no-group-title':!title}">
      <slot></slot>
    </div>
  </div>
</template>

<script>
import GroupTitle from '../group-title'

export default {
  components: {
    GroupTitle
  },
  props: {
    title: String,
    titleColor: String
  }
}
</script>

<style lang="less">
@import '../../styles/weui/widget/weui_cell/weui_access';
@import '../../styles/weui/widget/weui_cell/weui_cell_global';

.vux-no-group-title {
  margin-top:15px;
}
.weui_cells > a {
  color:#000;
}
</style>
