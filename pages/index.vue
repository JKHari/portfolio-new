<template>
  <div>
    <!-- this is a header  -->
    <section id="home-section" class="max-w-[1200px] mx-auto my-[70px]">
      <div class="flex">
        <!-- this is a content  -->
        <div class="w-1/2 h-auto">
          <div class="pl-[15px]">
            <p class="mt-6 text-5xl leading-normal text-[#3d3d3d] font-bold">
              Welcome to Hari Portfolio
            </p>
            <p class="mt-6 pr-[150px]">
              As a passionate and experienced Full Stack Developer, I am
              dedicated to solving complex problems and delivering high-quality
              solutions.
            </p>
            <button
              class="mt-[43px] px-4 py-2 rounded-md border-[#164085] text-[#164085] border-solid border-2 hover:mb-3 cursor-pointer hover:shadow-lg"
            >
              View Projects
            </button>
          </div>
        </div>
        <div class="w-[620px] h-[348px]">
          <img src="developer.webp" alt="" />
        </div>
      </div>
    </section>
    <!-- skills   -->
    <section
      id="skills-section"
      class="mx-auto max-w-[1200px] text-center py-[66px]"
    >
      <p class="text-3xl font-bold text-[#303030]">My Skills</p>
      <p class="pt-4 text-[#3d3d3d]">I specialize in the following areas:</p>
      <div class="flex mt-20">
        <div
          v-for="(logo, index) in logos"
          :key="index"
          class="flex gap-8 flex-wrap h-auto"
        >
          <div
            v-for="item in logo.img"
            :key="item"
            data-aos="fade-up"
            data-aos-duration="2000"
            class="h-40 w-40 bg-white shadow-md rounded-md flex justify-center items-center hover:shadow-xl cursor-pointer"
          >
            <img :src="item" alt="" class="h-20 w-20" />
          </div>
        </div>
      </div>
    </section>

    <!-- skills  -->
    <!-- <div class="mx-auto w-full text-center py-[66px]">
      <p class="text-3xl font-bold text-[#303030]">My Skills</p>
      <p class="pt-4 text-[#3d3d3d]">I specialize in the following areas:</p>
      
      <div
        class="flex flex-wrap justify-center gap-[30px] text-start mt-[51px] mx-[220px]"
      >
        <div v-for="(skill, index) in skills" :key="index" class=" ">
          <div class="rounded-md shadow-md px-[25px]">
            <div class="pt-[30px]">
              <img :src="skill.img" alt="" class="h-10 w-10" />
            </div>
            <h1 class="pt-[15px] font-bold text-lg text-[#303030]">
              {{ skill.title }}
            </h1>
            <p class="pt-[10px] text-[#3d3d3d] leading-normal pb-10">
              {{ skill.content }}
            </p>
          </div>
        </div>
      </div>
    </div> -->

    <!-- <div class="w-full flex justify-center items-center">
      <div data-aos="fade-up" data-aos-duration="3000">
        <div class="w-40 h-40 bg-green-300">hello aos</div>
      </div>
    </div> -->

    <!-- experience  -->
    <section id="experience-section" class="mt-20 mx-auto max-w-[1200px]">
      <div class="w-full flex justify-center">
        <p class="text-3xl font-bold text-[#303030]">My Experience</p>
      </div>
      <div class="flex mt-20">
        <div data-aos="fade-right" class="w-1/2">
          <img src="code1.png" alt="" />
        </div>
        <div class="flex gap-4 w-1/2">
          <div class="flex flex-col items-center justify-center">
            <p class="rounded-full border border-gray-200 px-3 py-1">1</p>
            <span class="h-full w-[2px] bg-gray-200"></span>
          </div>
          <!-- <div class="flex flex-col items-center justify-center">
            <p class="rounded-full border border-gray-200 px-3 py-1">1</p>
            <span class="h-full w-1 bg-gray-200 animate-loading"></span>
          </div> -->
          <!-- <div class="flex flex-col">
            <div class="flex flex-col items-center justify-center">
              <p class="rounded-full border border-gray-200 px-3 py-1">1</p>
            </div>
            <div class="flex flex-col items-center justify-center">
              <span class="loading-bar"></span>
            </div>
          </div> -->
          <div data-aos="fade-left" class="pl-2">
            <h1 class="text-2xl font-bold text-[#303030]">
              Full stack Developer
            </h1>
            <p class="mt-3 text-lg font-normal text-gray-400">
              Jul 2022- Present
            </p>
            <p class="mt-3 text-lg font-normal text-gray-400">
              Lmes Academy , Chennai
            </p>
            <p class="mt-4 text-black/80">
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
          class="flex flex-wrap p-3 justify-center px-[15%] w-full"
        >
          <div class="p-3 flex gap-[5%] w-full">
            <div class="w-1/2">
              <img :src="project.img" alt="image" class="w-[500px] h-[330px]" />
            </div>
            <div class="w-1/2">
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
  height: 1px; /* Start with a height of 1 pixel */
  width: 1px; /* You can set this to any initial width you prefer */
  background-color: #c4c8cf;
  animation: expandHeight 12s forwards;
}

@keyframes expandHeight {
  0% {
    height: 1px; /* Start with 1 pixel height */
  }
  100% {
    height: 300px; /* End with 300 pixels height */
  }
}
</style>
