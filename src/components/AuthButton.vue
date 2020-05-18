<template>
  <div
    class="btn-group"
    role="group"
    aria-label="Button group with nested dropdown"
  >
    <button
      type="submit"
      id="sendlogin"
      class="btn btn-primary d-flex justify-content-center align-items-center"
      style="width:100%"
    >
      <h1 class="display-4" style="font-size: 2rem;">Login</h1>
    </button>
    <button
      type="submit"
      id="sendlogin"
      class="btn btn-primary d-flex justify-content-center align-items-center"
      style="width:100%"
    >
      <div class="loader" v-if="loading"></div>
      <Icon
        v-else
        name="caret-right-fill"
        color="#ffffff"
        fontSize="1.5rem"
        width="auto"
      />
    </button>
  </div>
</template>

<script>
import Icon from '@/components/Icon.vue'
export default {
  name: 'AuthButton',
  components: { Icon },
  props: {
    username: {
      type: String,
      default: ''
    },
    password: {
      type: String,
      default: ''
    }
  },
  data() {
    return {
      loading: false
    }
  }
}
</script>

<style>
.loader {
  font-size: 4px;
  width: 8em;
  height: 8em;
  border-radius: 50%;
  background: #ffffff;
  background: linear-gradient(
    to right,
    #ffffff 10%,
    rgba(255, 255, 255, 0.24) 42%
  );
  position: relative;
  -webkit-animation: load3 1.4s infinite linear;
  animation: load3 1.4s infinite linear;
  transform: translateZ(0);
}
.loader:before {
  width: 50%;
  height: 50%;
  background: #ffffff;
  border-radius: 100% 0 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}
.loader:after {
  background: #007bff;
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}
@-webkit-keyframes load3 {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}
@keyframes load3 {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}
</style>
