<template>
  <nav class="navbar navbar-expand-lg bg-primary">
    <div class="container-fluid">
      <RouterLink to="/"><a class="navbar-brand">Text Utils</a></RouterLink>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <RouterLink to="/"
              ><a class="nav-link active" aria-current="page"
                >Home</a
              ></RouterLink
            >
          </li>
          <li class="nav-item">
            <RouterLink to="/about"><a class="nav-link">About</a></RouterLink>
          </li>
          <li class="nav-item dropdown">
            <a
              class="nav-link dropdown-toggle"
              href="#"
              role="button"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              Dropdown
            </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="#">Action</a></li>
              <li><a class="dropdown-item" href="#">Another action</a></li>
              <li>
                <hr class="dropdown-divider" />
              </li>
              <li><a class="dropdown-item" href="#">Something else here</a></li>
            </ul>
          </li>
          <li class="nav-item">
            <a class="nav-link disabled">Disabled</a>
          </li>
        </ul>
        <form class="d-flex" role="search">
          <input
            class="form-control me-2"
            type="search"
            placeholder="Search"
            aria-label="Search"
          />
          <button class="btn btn-outline-success" type="submit">Search</button>
        </form>
      </div>
    </div>
  </nav>
</template>

<script lang="ts">
import { RouterLink, RouterView } from "vue-router";
export default {
  name: "Navbar",
};
</script>

<style scoped>
a {
  text-decoration: none;
}

.nav-link {
  color: rgb(228, 228, 228);
}

.active,
.navbar-brand {
  color: white !important;
  font-weight: 600;
}

.navbar-brand {
  font-size: 1.5rem;
}
</style>
