<!--
 * @Author: wanggaoxian mlabor@163.com
 * @Date: 2024-11-26 19:43:41
 * @LastEditors: Please set LastEditors
 * @LastEditTime: 2024-11-28 09:47:40
 * @FilePath: /vue3/src/App.vue
 * @Description: 这是默认设置,可以在设置》工具》File Description中进行配置
 -->
<template>
  <div class="">
    <div class="">
      <h1>123123123123</h1>
      <el-input v-model="count"></el-input>
      <el-form ref="loginFormRef" class="login-form" :model="loginFormData" label-position="top">
        <!-- 邮箱 -->
        <el-form-item prop="email" label="ユーザーID">
          <el-input v-model.trim="loginFormData.email" placeholder="ユーザIDを入力してください" size="large" class="h-[48px]" :maxlength="254" />
        </el-form-item>
        <!-- 密码 -->
        <el-form-item prop="password" label="パスワード" class="mt-[36px]">
          <el-input v-model.trim="loginFormData.password" placeholder="パスワードを入力してください" type="password" name="password" size="large" show-password class="h-[48px]" />
        </el-form-item>
        <!-- 登录按钮 -->
        <el-button :loading="loading" type="primary" size="large" class="w-full login-btn" >ログイン</el-button>
        <!-- 忘记密码 -->
        <div class="forget-password" >パスワードを忘れた場合</div>
      </el-form>

      <!--      <h1>{{ count }}</h1>-->
      <!--      <h1>{{ duble }}</h1>-->
      <!--      <button @click="increase">按钮</button>-->
      <!--      &lt;!&ndash; <button @click="duble">按钮</button> &ndash;&gt;-->
      <!--      <ul>-->
      <!--        <li v-for="item in numbers" :key="item">{{ item }}</li>-->
      <!--      </ul>-->
      <!--      <h1>{{ persom.name }}</h1>-->
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import { ElInput } from "element-plus";

const count = ref("123123");
const loginFormData = ref({
  email: "user1@example.com",
  password: "password1",
});

// export default {
//   name: "App",
//   setup() {
//     // const count = ref(0);
//     // const duble = computed(() => {
//     //   return count.value * 2;
//     // });
//     // const increase = () => {
//     //   count.value++;
//     // };
//     const data: DateProps = reactive({
//       count: 0,
//       increase: () => {
//         data.count++;
//       },
//       duble: computed(() => data.count * 2),
//       numbers: [1, 2, 3],
//       persom: {},
//     });
//     const refs = toRefs(data);
//     data.numbers[0] = 5;
//     data.persom.name = "prosm";
//     return {
//       // count,
//       // increase,duble
//       // ...refs,
//     };
//   },
// };
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
