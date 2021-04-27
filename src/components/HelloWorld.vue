<template>
  <div class="hello">
    <ElInputTree
      v-model="id"
      checkStrictly
      placeholder="请选择"
      clearable
      :props="props"
      :dic="treeData"
    ></ElInputTree>
  </div>
</template>

<script>
import ElInputTree from "./el-input-tree";
export default {
  name: "HelloWorld",
  components: {
    ElInputTree,
  },
  data() {
    return {
      id: "",
      props: {
        label: "label",
        value: "value",
        children: "children",
      },
      treeData: [
        {
          label: "测试",
          value: 1,
          children: [
            {
              label: "测试2",
              value: 2,
              children: [],
            },
            {
              label: "测试3",
              value: 3,
              children: [],
            },
          ],
        },
        {
          label: "测试4",
          value: 4,
          children: [
            {
              label: "测试5",
              value: 5,
              children: [],
            },
            {
              label: "测试6",
              value: 6,
              children: [],
            },
          ],
        },
        {
          label: "测试7",
          value: 7,
          children: [],
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
