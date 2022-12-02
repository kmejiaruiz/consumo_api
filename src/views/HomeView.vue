<template>
  <div class="background">
    <div class="text">
      <h4>
        Getting Started <br />
        Welcome to our page on Vue.JS!
      </h4>
      <div class="intermedio"></div>
      <div class="boton">
        <button
          type="button"
          class="btn btn-light col-12 col-md-12"
          data-bs-toggle="modal"
          data-bs-target="#exampleModalToggle"
        >
          Ver proyectos realizados
        </button>
      </div>
    </div>
  </div>
  <div
    class="modal fade"
    id="exampleModalToggle"
    tabindex="-1"
    aria-labelledby="exampleModalLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h1 class="modal-title fs-5" id="exampleModalLabel">
            Explora nuestros proyectos
          </h1>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body">
          <div class="ratio ratio-1x1">
            <iframe
              src="https://kmejiaruiz.github.io/prematricula"
              frameborder="0"
            ></iframe>
          </div>
        </div>
        <div class="modal-footer">
          <button
            class="btn btn-primary"
            data-bs-target="#exampleModalToggle2"
            data-bs-toggle="modal"
          >
            Ir a segunda vista
          </button>
        </div>
      </div>
    </div>
  </div>
  <div
    class="modal fade"
    id="exampleModalToggle2"
    aria-hidden="true"
    aria-labelledby="exampleModalToggleLabel2"
    tabindex="-1"
  >
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h1 class="modal-title fs-5" id="exampleModalToggleLabel2">
            Segunda vista
          </h1>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body">
          <div class="ratio ratio-1x1">
            <iframe src="https://kmejiaruiz.github.io/login_propio/" frameborder="0"></iframe>
          </div>
        </div>
        <div class="modal-footer">
          <button
            class="btn btn-primary"
            data-bs-target="#exampleModalToggle"
            data-bs-toggle="modal"
          >
            Volver a vista anterior
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.background {
  background: url("../img/pokeapi_cover.jpg") 50% 50% no-repeat;
  background-size: cover;
  position: relative;
  height: 88.5vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.background:before {
  width: 100%;
  content: " ";
  background-color: rgba(0, 0, 0, 0.658);
  position: absolute;
  top: 0px;
  z-index: 1;
  left: 0;
  height: 100%;
}
.text {
  width: 50%;
  z-index: 1;
  text-align: center;
  color: #fff;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 15px;
}
.intermedio {
  width: 1.5px;
  display: flex;

  background: #000000;
  background: linear-gradient(
    180deg,
    #020024 0%,
    #e60b0b 30%,
    #cfd70d 50%,
    #0b38bc 70%,
    #000000 100%
  );
  z-index: 99;
  height: 88.5vh;
  gap: -5px;
  /* position: relative; */
}
body {
  overflow: hidden;
}
.text h4 {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  font-style: bold;
}
.text h5 {
  text-align: center;
}
@media (max-width: 750px) {
  .text {
    flex-direction: column;
    justify-content: center !important;
    width: 100%;
  }
  .intermedio {
    flex-direction: column;
    height: 1px;
    width: 100% !important;
    background: rgb(0, 0, 0);
    background: linear-gradient(
      90deg,
      rgba(2, 0, 36, 1) 0%,
      rgba(230, 11, 11, 1) 30%,
      rgba(207, 215, 13, 1) 50%,
      rgba(11, 56, 188, 1) 70%,
      rgba(0, 0, 0, 1) 100%
    ) !important;
  }
}
@media (max-width: 210px) {
  .background {
    background: #000;
  }
}
</style>