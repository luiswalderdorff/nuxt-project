<template>
  <div>
    <nav class="navbar navbar-expand-md navbar-dark bg-dark px-5">
      <a class="navbar-brand" href="#">Nuxt</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarsExampleDefault"
              aria-controls="navbarsExampleDefault" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarsExampleDefault">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
            <a class="nav-link" href="/">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="/overview">Overview</a>
          </li>
        </ul>
      </div>
    </nav>

    <main role="main">

      <NuxtPage/>
      <hr>
    </main>

    <footer class="container">
      <p>© Nuxt 2023</p>
    </footer>
  </div>
</template>
