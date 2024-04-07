
  <template>
    <body class="bg-pink-300">

      <section class="flex flex-col sm:justify-between items-center sm:flex-row mt-12 sm:mt-10 ">
        <!-- Banner left contents -->
        <div class="w-full md:w-1/3 text-left">
          <h1 class="font-general-semibold text-3xl md:text-3xl xl:text-4xl text-center sm:text-center text-ternary-dark uppercase">
           Honey Cuizon.
          </h1>
          <p class="font-general-semibold text-sm text-center sm:text-center text-ternary-dark">Portfolio</p>
        </div>

        <!-- Banner right illustration -->
        <div class="w-50 md:w-2/3 text-right float-right">
          <img src="@/assets/images/hani.jpg" alt="Anna" class="anna" />
        </div>
      </section>
      <router-view></router-view>
      </body>
  </template>

  <style scoped>
    .anna {
      width: 250px;
      height: 250px;
      margin-left: 20%;
    }

  </style>
