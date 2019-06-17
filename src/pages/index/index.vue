<template>
  <simple-wrapper>
    <view v-for="ia in nestList" :key="ia.name">
      <view>{{ia.name}}</view>
      <view v-for="ib in ia.value" :key="ib">-{{ib}}</view>
    </view>
  </simple-wrapper>
</template>

<script>
  import SimpleWrapper from "../../components/simpleWrapper.vue";
  export default {
    components: {
      SimpleWrapper
    },
    data() {
      return {
        nestList: [
          {name: "a", value: ["a1", "a2"]},
          {name: "b", value: ["b1", "b2"]}
        ]
      }
    }
  }
</script>