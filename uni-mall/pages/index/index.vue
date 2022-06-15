<template>
  <view class="msg">
    <text class="text1">{{ msg }}</text>
    <button @click="change">点击我</button>
    <input v-model="msg" />
    <view v-if="flag">条件判断：{{ msg }}</view>
    <view v-else>条件判断else</view>

    <view v-for="itemx in arr" :key="itemx">{{ itemx }}</view>
    <view v-for="(value, key) in obj" :key="key">{{ key }}--{{ value }}</view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      msg: "Oral",
      flag: false,
      arr: [1, 2, 3],
      obj: {
        name: "a",
        age: 23,
      },
    };
  },
  onLoad() {
    setTimeout(() => {
      this.msg = "oral2";
    }, 3000);
  },
  methods: {
    change() {
      this.msg = "zhang";
      this.flag = !this.flag;
    },
  },
};
</script>

<style lang="scss">
	.msg{
		color: #f00;
		.text1{
			color: #00f;
		}
	}
</style>
