<template>
  <div class="max-w-7xl m-center pt-48">
    <div
      class="skills text-center mt-10"
      data-aos="fade-up"
      data-aos-delay="100"
      data-aos-duration="800"
    >
      <h2 class="text-5xl dark:text-white">Skills</h2>
      <span class="f-gray text-sm dark:text-white">My Technical Level</span>
    </div>
    <div class="skill-details flex mt-20 flex-col lg:flex-row lg:gap-10">
      <div
        data-aos="fade-down"
        data-aos-duration="1000"
        data-aos-delay="200"
        class="lg:w-1/3 md:w-96 md:m-auto md:mb-16 card bg-white drop-shadow-2xl dark:bg-slate-800"
      >
        <h2 class="pt-7 pl-5 flex items-center">
          <font-awesome-icon
            class="fa-2xl pr-3 f-blue w-20"
            :icon="['fas', 'code']"
          />
          <div class="flex flex-col">
            <h2 class="text-xl dark:text-white">BI Developer</h2>
            <span class="text-sm f-gray dark:text-white"
              >More than 1 year</span
            >
          </div>
        </h2>
        <div
          class="description grid grid-cols-4 gap-4 m-auto lg:px-10 px-5 pt-10"
        >
          <div class="p-1 card-mini">
            <img
              src="https://upload.wikimedia.org/wikipedia/en/thumb/2/20/Power_BI_logo.svg/70px-Power_BI_logo.svg.png"
              class="h-14"
              alt="PowerBI"
            />
            <span class="dark:text-white">Power Bi</span>
          </div>
          <div class="p-1 card-mini">
            <img
              src="https://seeklogo.com/images/E/excel-logo-974BFF9CB9-seeklogo.com.png"
              class="h-14"
              alt="EXCEL"
            />
            <span class="dark:text-white">Excel</span>
          </div>
          <div class="p-1 card-mini">
            <img
              src="https://www.gstatic.com/images/branding/product/1x/sheets_2020q4_48dp.png"
              class="h-14"
              alt="Google Sheet"
            />
            <span class="dark:text-white">Google Sheet</span>
          </div>
        </div>
      </div>
      <div
        data-aos="fade-down"
        data-aos-duration="1000"
        data-aos-delay="400"
        class="lg:w-1/3 md:w-96 md:m-auto md:mb-16 card bg-white drop-shadow-2xl dark:bg-slate-800"
      >
        <h2 class="pt-7 pl-5 flex items-center">
          <font-awesome-icon
            class="fa-2xl pr-3 f-blue w-20"
            :icon="['fas', 'code-branch']"
          />
          <div class="flex flex-col">
            <h2 class="text-xl dark:text-white">Backend Developer</h2>
            <span class="text-sm f-gray dark:text-white"
              >More than 1 year</span
            >
          </div>
        </h2>
        <div
          class="description grid grid-cols-4 gap-4 m-auto lg:px-10 px-5 pt-10"
        >
          <div class="p-1 card-mini">
            <img
              src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/121px-Python-logo-notext.svg.png"
              class="h-14"
              alt="Python"
            />
            <span class="dark:text-white">Python</span>
          </div>
          <div class="p-1 card-mini">
            <img
              src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Postgresql_elephant.svg/120px-Postgresql_elephant.svg.png"
              class="h-14"
              alt="Posgresql"
            />
            <span class="dark:text-white">PosgreSQL</span>
          </div>
          <div class="p-1 card-mini">
            <img
              src="https://www.freepnglogos.com/uploads/logo-mysql-png/logo-mysql-mysql-logo-png-images-are-download-crazypng-21.png"
              class="h-14"
              alt="Mysql"
            />
            <span class="dark:text-white">Mysql</span>
          </div>
          <div class="p-1 card-mini">
            <img
              src="https://www.sqlite.org/images/sqlite370_banner.gif"
              class="h-14"
              alt="AWS"
            />
            <span class="dark:text-white">SQLite 3</span>
          </div>
          <div class="p-1 card-mini">
            <img
              src="https://jupyter.org/assets/logos/rectanglelogo-greytext-orangebody-greymoons.svg"
              class="h-14"
              alt="jupy"
            />
            <span class="dark:text-white">Jupyter Notebook</span>
          </div>
        </div>
      </div>
      <div
        data-aos="fade-down"
        data-aos-duration="1000"
        data-aos-delay="600"
        class="lg:w-1/3 md:w-96 md:m-auto md:mb-16 card bg-white drop-shadow-2xl dark:bg-slate-800"
      >
        <h2 class="pt-7 pl-5 flex items-center">
          <font-awesome-icon
            class="fa-2xl pr-3 f-blue w-20"
            :icon="['fas', 'brain']"
          />
          <div class="flex flex-col">
            <h2 class="text-xl dark:text-white">Others</h2>
            <span class="text-sm f-gray dark:text-white">Acquired Skills</span>
          </div>
        </h2>
        <div
          class="description grid grid-cols-4 gap-4 m-auto lg:px-10 px-5 pt-10"
        >
          <div class="p-1 card-mini">
            <img
              src="https://seeklogo.com/images/G/github-logo-5F384D0265-seeklogo.com.png"
              class="h-14"
              alt="Git"
            />
            <span class="dark:text-white">Git</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
