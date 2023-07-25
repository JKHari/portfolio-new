<template>
  <div>
    <!-- this is a header  -->
    <section id="home-section" class="max-w-[1200px] mx-auto my-[70px] w-full">
      <div class="flex flex-col lg:flex-row items-center justify-center">
        <!-- this is a content  -->
        <div class="w-full lg:w-1/2 h-auto px-3 md:px-10 text-center">
          <div class="pl-[15px]">
            <p
              class="mt-6 text-3xl lg:text-5xl leading-normal text-[#3d3d3d] font-bold"
            >
              Welcome to Hari Portfolio
            </p>
            <p class="mt-6 lg:pr-[150px]">
              As a passionate and experienced Full Stack Developer, I am
              dedicated to solving complex problems and delivering high-quality
              solutions.
            </p>

            <div class="w-full flex items-center justify-center">
              <a
                href="#projects-section"
                class="block mt-[43px] px-4 py-2 rounded-md border-[#164085] text-[#164085] border-solid border-2 text-center cursor-pointer hover:shadow-2xl w-36"
              >
                View Projects
              </a>
            </div>
          </div>
        </div>
        <!--  -->
        <div class="w-full px-5 max-w-[620px] max-h-[348px] mt-20">
          <img src="/you.png" alt="" class="rounded-xl w-[100%] h-auto" />
        </div>
      </div>
    </section>
    <!-- skills   -->
    <section
      id="skills-section"
      class="mx-auto max-w-[1200px] text-center py-[66px] w-full px-10"
    >
      <p class="text-3xl font-bold text-[#303030]">My Skills</p>
      <p class="pt-4 text-[#3d3d3d]">I specialize in the following areas:</p>
      <div class="flex mt-10 md:mt-20">
        <div
          v-for="(logo, index) in logos"
          :key="index"
          class="flex gap-8 flex-wrap h-auto justify-center"
        >
          <div
            v-for="item in logo.img"
            :key="item"
            data-aos="fade-up"
            data-aos-duration="2000"
            md:data-aos-duration="3000"
            class="h-32 w-32 md:h-40 md:w-40 bg-white shadow-md rounded-md flex justify-center items-center hover:shadow-xl cursor-pointer"
          >
            <img :src="item" alt="" class="h-20 w-20" />
          </div>
        </div>
      </div>
    </section>

    <!-- experience  -->
    <section
      id="experience-section"
      class="mt-20 mx-auto w-full max-w-[1200px]"
    >
      <div class="w-full flex justify-center">
        <p class="text-3xl font-bold text-[#303030]">My Experience</p>
      </div>
      <div class="w-full flex flex-col lg:flex-row mt-20 items-center px-5 md:px-10">
        <div md:data-aos="fade-right" class="w-full lg:w-1/2">
          <img src="/code1.png" alt="" class="w-[100%] h-auto" />
        </div>
        <div class="flex gap-4 w-full lg:w-1/2 px-3 mt-4 md:mt-0 md:px-10">
          <div
            class="hidden lg:block flex flex-col items-center justify-center"
          >
            <p class="rounded-full border border-gray-200 px-3 py-1">1</p>
            <span class="h-full w-[2px] bg-gray-200"></span>
          </div>

          <div md:data-aos="fade-left" class="pl-2 mt-4">
            <h1 class="text-xl md:text-2xl font-bold text-[#303030]">
              Full stack Developer
            </h1>
            <p
              class="mt-2 md:mt-3 text-md md:text-lg font-normal text-gray-400"
            >
              Jul 2022- Present
            </p>
            <p
              class="mt-2 md:mt-3 text-md md:text-lg font-normal text-gray-400"
            >
              Lmes Academy , Chennai
            </p>
            <p class="mt-2 md:mt-4 text-md text-black/80">
              As a proficient full stack developer at LMES Academy , I have
              played a vital role in a diverse range of projects, including
              designing and implementing Role-Based Access Control (RBAC)
              systems, optimizing databases using SQL/MySQL, and building
              user-friendly websites with NUXT 3. Collaborating seamlessly with
              cross-functional teams, I take pride in delivering clean code
              architecture, ensuring scalability and security while staying
              updated with the latest industry trends. With a passion for
              problem-solving and continuous learning, I am committed to
              creating impactful and efficient web solution
            </p>
            <div>
              <p></p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- project  -->
    <section id="projects-section" class="w-full mx-auto max-w-[1200px] mt-20">
      <div class="flex justify-center">
        <p class="text-3xl font-bold text-[#303030]">My Recent Project</p>
      </div>
      <!-- project sections -->
      <div class="w-full pt-[60px]">
        <div
          data-aos="fade-up"
          data-aos-duration="3000"
          v-for="(project, index) in projects"
          :key="index"
          class="flex flex-wrap p-3 justify-center lg:px-[15%] w-full px-20"
        >
          <div class="p-3 flex flex-col gap-[5%] w-full">
            <div class="w-full lg:w-1/2">
              <img :src="project.img" alt="image" class="w-[500px] h-[330px]" />
            </div>
            <div class="w-full lg:w-1/2 mt-4 lg:mt-0">
              <p class="pt-[15px] text-2xl font-bold text-[#303030]">
                {{ project.heading }}
              </p>
              <p class="pt-[20px]">{{ project.content }}</p>
              <div
                class="pt-[20px] hover:text-[#14b8a6] transition duration-150"
              >
                <a :href="project.link" class="flex gap-2">
                  <img :src="project.linkimg" class="w-5 h-5" /> View Project
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <div
      class="w-full bg-[#303030] h-[300px] flex items-center justify-center mt-10"
    >
      <div class="w-full flex flex-col justify-center items-center">
        <p
          class="text-3xl font-bold text-white hover:text-white/90 cursor-pointer"
        >
          Contact
        </p>
        <div class="flex gap-5 mt-5">
          <div
            v-for="(data, index) in socialmedia"
            :key="index"
            class="flex flex-row gap-3 mt-5 p-2"
          >
            <a :href="data.link" target="black" class="">
              <img :src="data.img" alt="" class="h-7 w-7" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AOS from "aos";
import "aos/dist/aos.css";
import { logos, socialmedia, skills, projects } from "./store";
export default {
  data() {
    return {
      logos,
      socialmedia,
      skills,
      projects,
    };
  },
  mounted() {
    AOS.init();
  },
};
</script>
<style>
.loading-bar {
  height: 1px;
  width: 1px;
  background-color: #c4c8cf;
  animation: expandHeight 12s forwards;
}

@keyframes expandHeight {
  0% {
    height: 1px;
  }
  100% {
    height: 300px; /* End with 300 pixels height */
  }
}
</style>
