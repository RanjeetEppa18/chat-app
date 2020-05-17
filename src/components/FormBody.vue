<template>
  <div class="d-flex flex-item-center align-items-center">
    <hr class="style-two" />
    <div class="form-group">
      <div class="input-group mb-3">
        <div class="input-group-prepend">
          <span class="input-group-text" id="basic-addon1">
            <svg
              style="font-size: 1.2rem;"
              class="bi bi-person"
              width="1em"
              height="1em"
              viewBox="0 0 16 16"
              fill="currentColor"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M13 14s1 0 1-1-1-4-6-4-6 3-6 4 1 1 1 1h10zm-9.995-.944v-.002.002zM3.022 13h9.956a.274.274 0 00.014-.002l.008-.002c-.001-.246-.154-.986-.832-1.664C11.516 10.68 10.289 10 8 10c-2.29 0-3.516.68-4.168 1.332-.678.678-.83 1.418-.832 1.664a1.05 1.05 0 00.022.004zm9.974.056v-.002.002zM8 7a2 2 0 100-4 2 2 0 000 4zm3-2a3 3 0 11-6 0 3 3 0 016 0z"
                clip-rule="evenodd"
              />
            </svg>
          </span>
        </div>
        <input
          type="text"
          class="form-control"
          placeholder="username"
          aria-label="Username"
          aria-describedby="basic-addon1"
        />
      </div>
    </div>
    <div class="form-group">
      <div class="input-group mb-3">
        <input
          type="password"
          class="form-control"
          placeholder="password"
          name="password"
        />
        <div class="input-group-append">
          <span class="input-group-text" id="basic-addon1">
            <svg
              style="font-size: 1.2rem;"
              class="bi bi-eye-slash"
              width="1em"
              height="1em"
              viewBox="0 0 16 16"
              fill="currentColor"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M13.359 11.238C15.06 9.72 16 8 16 8s-3-5.5-8-5.5a7.028 7.028 0 00-2.79.588l.77.771A5.944 5.944 0 018 3.5c2.12 0 3.879 1.168 5.168 2.457A13.134 13.134 0 0114.828 8c-.058.087-.122.183-.195.288-.335.48-.83 1.12-1.465 1.755-.165.165-.337.328-.517.486l.708.709z"
              />
              <path
                d="M11.297 9.176a3.5 3.5 0 00-4.474-4.474l.823.823a2.5 2.5 0 012.829 2.829l.822.822zm-2.943 1.299l.822.822a3.5 3.5 0 01-4.474-4.474l.823.823a2.5 2.5 0 002.829 2.829z"
              />
              <path
                d="M3.35 5.47c-.18.16-.353.322-.518.487A13.134 13.134 0 001.172 8l.195.288c.335.48.83 1.12 1.465 1.755C4.121 11.332 5.881 12.5 8 12.5c.716 0 1.39-.133 2.02-.36l.77.772A7.029 7.029 0 018 13.5C3 13.5 0 8 0 8s.939-1.721 2.641-3.238l.708.709z"
              />
              <path
                fill-rule="evenodd"
                d="M13.646 14.354l-12-12 .708-.708 12 12-.708.708z"
                clip-rule="evenodd"
              />
            </svg>
          </span>
        </div>
      </div>
    </div>
    <button
      type="button"
      id="sendlogin"
      class="btn btn-primary d-flex justify-content-center align-items-center"
    >
      <h1 class="display-4" style="font-size: 2rem;">Login</h1>
      <svg
        class="bi bi-check"
        width="1em"
        height="1em"
        viewBox="0 0 16 16"
        fill="currentColor"
        xmlns="http://www.w3.org/2000/svg"
        style="font-size: 2rem; color: #07df32;"
      >
        <path
          fill-rule="evenodd"
          d="M13.854 3.646a.5.5 0 010 .708l-7 7a.5.5 0 01-.708 0l-3.5-3.5a.5.5 0 11.708-.708L6.5 10.293l6.646-6.647a.5.5 0 01.708 0z"
          clip-rule="evenodd"
        />
      </svg>
    </button>
    <hr class="style-two" />
  </div>
</template>

<script>
export default {
  name: 'FormBody'
}
</script>

<style></style>
