<template>
  <div class="body">
    <div class="container">
      <div class="blueBg">
        <div class="box signin">
          <h2>已经有账号了?</h2>
          <button @click="signIn">登录</button>
        </div>
        <div class="box signup">
          <h2>没有账号吗?</h2>
          <button @click="signUp">注册</button>
        </div>
      </div>
      <div class="formBX"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  components: {},
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      list: [1, 2, 3, 4, 5],
      formBx: null,
      body: null
    };
  },
  mounted() {
    this.formBx = document.querySelector(".formBX");
    this.body = document.querySelector(".body");
  },
  methods: {
    signUp() {
      console.log(this.formBx);
      this.formBx.classList.add("active");
      this.body.classList.add("active");
    },
    signIn() {
      console.log(this.formBx);
      this.formBx.classList.remove("active");
      this.body.classList.remove("active");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.body {
  display: flex;
  background-color: #03a9f4;
  position: fixed;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  transition: 0.5s;
}
.body.active {
  background: #f43648;
}
.container {
  position: relative;
  width: 800px;
  height: 500px;
  margin: 20px;
}
.blueBg {
  position: absolute;
  top: 40px;
  width: 100%;
  height: 420px;
  display: flex;
  justify-content: center;
  align-items: center;
  background: rgba(255, 255, 255, 0.2);
  box-shadow: 0 5px 45px rgba(0, 0, 0, 0.15);
  border-radius: 12px;
}
.box {
  position: relative;
  width: 50%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.box h2 {
  color: #fff;
  font-size: 1.5em;
  font-weight: 700;
  margin-bottom: 10px;
}

.box button {
  cursor: pointer;
  padding: 10px;
  background: #fff;
  color: #333;
  font-size: 16px;
  font-weight: 700;
  border: none;
  border-radius: 8px;
}

.formBX {
  position: absolute;
  top: 0;
  left: 0;
  width: 50%;
  height: 100%;
  background: #fff;
  z-index: 1000;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0 5px 45px rgba(0, 0, 0, 0.25);
  transition: 0.5s ease-in-out;
  border-radius: 12px;
}

.formBX.active {
  left: 50%;
}
</style>
