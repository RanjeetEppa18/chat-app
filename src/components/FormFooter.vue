<template>
  <div>
    <button
      disabled="true"
      class="disabled firebaseui-idp-button mdl-button mdl-js-button mdl-button--raised firebaseui-idp-google firebaseui-id-idp-button"
      data-provider-id="google.com"
      style="background-color:#ffffff"
      data-upgraded=",MaterialButton"
    >
      <span class="firebaseui-idp-icon-wrapper">
        <img
          class="firebaseui-idp-icon"
          alt
          src="https://www.gstatic.com/firebasejs/ui/2.0.0/images/auth/google.svg"
        />
      </span>
      <span class="firebaseui-idp-text firebaseui-idp-text-long"
        >Sign in with Google</span
      >
      <span class="firebaseui-idp-text firebaseui-idp-text-short">Google</span>
    </button>
  </div>
</template>

<script>
export default {
  name: 'FormFooter'
}
</script>

<style></style>
