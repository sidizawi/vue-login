<template>
  <div id="app">
    <div class="login-box">
      <h2>Login</h2>
      <form>
        <div class="user-box">
          <input type="text" name="username" id="username">
          <label for="username">Username</label>
        </div>
        <div class="user-box">
          <input type="password" name="password" id="password">
          <label for="password">Password</label>
        </div>
        <a href="#">
          <span></span>
          <span></span>
          <span></span>
          <span></span>
          Submit
        </a>
      </form>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
}
</script>

<style>
html {
  height: 100%;
}

body {
  margin: 0;
  padding: 0;
  font-family: sans-serif;
  background: linear-gradient(#141e30, #243b55);
}

.login-box {
  position: absolute;
  top: 50%;
  left: 50%;
  padding: 40px;
  width: 400px;
  background-color: rgba(0, 0, 0, .5);
  box-sizing: border-box;
  border-radius: 10px;
  box-shadow: 0 15px 25px rgba(0, 0, 0, .6);
  transform: translate(-50%, -50%);
}

.login-box h2 {
  margin: 0 0 30px;
  padding: 0;
  color: #fff;
  text-align: center;
}

.user-box {
  position: relative;
}

.user-box input {
  width: 100%;
  padding: 10px 0;
  font-size: 16px;
  margin-bottom: 30px;
  border: none;
  outline: none;
  border-bottom: 1px solid #fff;
  color: #fff;
  background: transparent;
}

.user-box label {
  position: absolute;
  top: 0;
  left: 0;
  padding: 10px 0;
  font-size: 16px;
  color: #fff;
  pointer-events: none;
  transition: .5s;
}

.user-box input:focus ~ label {
  top: -20px;
  left: 0;
  color: #03e9f4;
  font-size: 12px;
}

.login-box a {
  position: relative;
  display: inline-block;
  padding: 10px 20px;
  font-size: 16px;
  text-decoration: none;
  text-transform: uppercase;
  color: #03e9f4;
  overflow: hidden;
  transition: .4s;
  margin-top: 40px;
  letter-spacing: 4px;
}

.login-box a:hover {
  background-color: #03e9f4;
  color: #fff;
  box-shadow: 0 0 5px #03e9f4,
              0 0 25px #03e9f4,
              0 0 50px #03e9f4,
              0 0 100px #03e9f4;
}

.login-box a span {
  position: absolute;
  display: block;
}

.login-box a span:nth-child(1) {
  top: 0;
  left: -100%;
  width: 100%;
  height: 2px;
  background: linear-gradient(90deg, transparent, #03e9f4);
  animation: btn-span1 1s linear infinite;
}

@keyframes btn-span1 {
  0% {
    left: -100%;
  }
  50%, 100% {
    left: 100%;
  }
}

.login-box a span:nth-child(2) {
  top: -100%;
  right: 0;
  width: 2px;
  height: 100%;
  background: linear-gradient(180deg, transparent, #03e9f4);
  animation: btn-span2 1s linear infinite;
  animation-delay: .25s;
}

@keyframes btn-span2 {
  0% {
    top: -100%;
  }
  50%, 100% {
    top: 100%;
  }
}

.login-box a span:nth-child(3) {
  bottom: 0%;
  right: -100%;
  width: 100%;
  height: 2px;
  background: linear-gradient(270deg, transparent, #03e9f4);
  animation: btn-span3 1s linear infinite;
  animation-delay: .5s;
}

@keyframes btn-span3 {
  0% {
    right: -100%;
  }
  50%, 100% {
    right: 100%;
  }
}

.login-box a span:nth-child(4) {
  bottom: -100%;
  left: 0%;
  width: 2px;
  height: 100%;
  background: linear-gradient(0deg, transparent, #03e9f4);
  animation: btn-span4 1s linear infinite;
  animation-delay: .75s;
}

@keyframes btn-span4 {
  0% {
    bottom: -100%;
  }
  50%,100% {
    bottom: 100%;
  }
}

</style>
