<template>
  <div class="container">
    <div
      class="row justify-content-center align-items-center"
      style="height: 100vh;"
    >
      <div class="col-4">
        <div class="card">
          <div class="card-body">
            <form action autocomplete="off" class="d-flex flex-item-center">
              <FormHeader></FormHeader>
              <FormBody></FormBody>
              <FormFooter></FormFooter>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import FormHeader from '@/components/FormHeader.vue'
import FormFooter from '@/components/FormFooter.vue'
import FormBody from '@/components/FormBody.vue'
export default {
  components: {
    FormBody,
    FormFooter,
    FormHeader
  }
}
</script>

<style>
.flex-item-center {
  flex-direction: column;
  justify-content: center;
  text-align: center;
}
hr.style-two {
  border: 0;
  height: 1px;
  width: 100%;
  background-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0.15),
    rgba(0, 0, 0, 0.4),
    rgba(0, 0, 0, 0.15)
  );
}

.mdl-button {
  background: 0 0;
  border: none;
  border-radius: 2px;
  color: #000;
  position: relative;
  height: 36px;
  margin: 0;
  min-width: 64px;
  padding: 0 16px;
  display: inline-block;
  font-family: Roboto, Helvetica, Arial, sans-serif;
  font-size: 14px;
  font-weight: 500;
  text-transform: uppercase;
  line-height: 1;
  letter-spacing: 0;
  overflow: hidden;
  will-change: box-shadow;
  transition: box-shadow 0.2s cubic-bezier(0.4, 0, 1, 1),
    background-color 0.2s cubic-bezier(0.4, 0, 0.2, 1),
    color 0.2s cubic-bezier(0.4, 0, 0.2, 1);
  outline: 0;
  cursor: pointer;
  text-decoration: none;
  text-align: center;
  line-height: 36px;
  vertical-align: middle;
}

.mdl-button--raised {
  background: rgba(158, 158, 158, 0.2);
  box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 3px 1px -2px rgba(0, 0, 0, 0.2),
    0 1px 5px 0 rgba(0, 0, 0, 0.12);
}

.firebaseui-idp-button {
  direction: ltr;
  font-weight: bold;
  height: auto;
  line-height: normal;
  max-width: 220px;
  min-height: 40px;
  padding: 8px 16px;
  text-align: left;
  align-self: center;
  width: 100%;
}

.firebaseui-idp-icon-wrapper {
  display: table-cell;
  vertical-align: middle;
}

.firebaseui-idp-text.firebaseui-idp-text-long {
  display: table-cell;
}

.firebaseui-idp-google > .firebaseui-idp-text {
  color: #757575;
}

.firebaseui-idp-text {
  color: #fff;
  display: table-cell;
  font-size: 14px;
  padding-left: 16px;
  text-transform: none;
  vertical-align: middle;
}

.firebaseui-idp-text.firebaseui-idp-text-short {
  display: none;
}
.firebaseui-idp-icon {
  border: none;
  display: inline-block;
  height: 18px;
  vertical-align: middle;
  width: 18px;
}
</style>
