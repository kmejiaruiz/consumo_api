<template>
  <div>
    <nav
      class="navbar navbar-dark navbar-expand-lg"
      style="background-color: #930a18"
    >
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img
            src="@/img/pokemon1.png"
            alt=""
            srcset=""
            width="45px"
            height="45px"
          />
        </a>
        <div
          class="navbar-toggler"
          type="button"
          data-bs-toggle="offcanvas"
          data-bs-target="#staticBackdrop"
          aria-controls="staticBackdrop"
          style="border: none"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 16 16"
            width="23"
            height="23"
          >
            <path
              fill="#fff"
              fill-rule="evenodd"
              d="M1 2.75A.75.75 0 011.75 2h12.5a.75.75 0 110 1.5H1.75A.75.75 0 011 2.75zm0 5A.75.75 0 011.75 7h12.5a.75.75 0 110 1.5H1.75A.75.75 0 011 7.75zM1.75 12a.75.75 0 100 1.5h12.5a.75.75 0 100-1.5H1.75z"
            ></path>
          </svg>
        </div>
        <div
          class="offcanvas offcanvas-end text-white"
          data-bs-backdrop="static"
          tabindex="-1"
          id="staticBackdrop"
          aria-labelledby="staticBackdropLabel"
          style="background: rgba(0, 0, 0, 0.8);"
        >
          <div class="offcanvas-header">
            <h5 class="offcanvas-title" id="staticBackdropLabel"> </h5>
            <div type="button" data-bs-dismiss="offcanvas" aria-label="Close">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                width="26"
                height="26"
              >
                <path
                  fill="#fff"
                  fill-rule="evenodd"
                  d="M5.72 5.72a.75.75 0 011.06 0L12 10.94l5.22-5.22a.75.75 0 111.06 1.06L13.06 12l5.22 5.22a.75.75 0 11-1.06 1.06L12 13.06l-5.22 5.22a.75.75 0 01-1.06-1.06L10.94 12 5.72 6.78a.75.75 0 010-1.06z"
                ></path>
              </svg>
            </div>
          </div>
          <div class="offcanvas-body">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <router-link class="nav-link" to="/">Home</router-link>
              </li>
              <li class="nav-item">
                <router-link class="nav-link" to="/about">About</router-link>
              </li>
              <li class="nav-item">
                <router-link class="nav-link" to="/clients"
                  >Buscar en API</router-link
                >
              </li>
              <li class="nav-item">
                <router-link class="nav-link" to="/register"
                  >Registrarse</router-link
                >
              </li>
              <!-- <li class="nav-item">
                <a class="nav-link disabled">Disabled</a>
              </li> -->
            </ul>
            <a class="contenedor" href="https://pokeapi.co">
              <h6 class="legend">Powered by:</h6>

              <img
                src="@/img/pokeapi_256.png"
                alt=""
                srcset=""
                class="brand2"
              />
            </a>
          </div>
        </div>
      </div>
    </nav>
  </div>
  <router-view />
</template>

<style>
.contenedor {
  text-decoration: none !important;
  color: #fff !important;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  margin: 0;
  padding: 0;
}
.brand2 {
  width: 25%;
  height: 85%;
}

@media (max-width: 991px) {
  .brand2 {
    width: 50%;
    height: 15%;
  }
  .contenedor {
    flex-direction: column;
  }
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  /* color: #2c3e50; */
}
.legend {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0;
}

/* nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
} */

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
