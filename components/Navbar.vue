<template>
  <div>
    <div class="hidden lg:block">
      <div
        class="bg-white shadow-md flex justify-around h-16 items-center w-full"
      >
        <p class="font-bold cursor-pointer hover:text-black/60">
          Hari Fullstack Developer
        </p>
        <div class="flex gap-10">
          <p class="px-2 py-2 cursor-pointer hover:text-black/70">
            <a href="#home-section">Home</a>
          </p>
          <p class="px-2 py-2 cursor-pointer hover:text-black/70">
            <a href="#skills-section">Skills</a>
          </p>
          <p class="px-2 py-2 cursor-pointer hover:text-black/70">
            <a href="#experience-section">Experience</a>
          </p>
          <p class="px-2 py-2 cursor-pointer hover:text-black/70">
            <a href="#projects-section">Projects</a>
          </p>

          <p
            class="px-4 py-2 rounded-md border-[#164085] text-[#164085] border-solid border-2 cursor-pointer"
          >
            Hire Me
          </p>
        </div>
      </div>
    </div>
    <!-- mobile device -->
    <div class="lg:hidden w-full">
      <div
        class="bg-white shadow-md flex justify-between px-6 h-16 items-center w-full"
      >
        <p class="font-bold cursor-pointer hover:text-black/60">
          Hari Fullstack Developer
        </p>
        <div
          @click="open = !open"
          class="w-9 h-9 bg-[#ffffff] rounded-full shadow-md p-2 cursor-pointer flex items-center justify-center"
        >
          <img
            :src="open ? '/menu-show.svg' : '/menu-hide.png'"
            alt=""
            class="w-full h-full"
          />
        </div>
      </div>
      <div v-if="!open" class="bg-white ">
        <div class="flex flex-col items-center justify-center mt-5 gap-10">
          <p
            class="px-2 cursor-pointer hover:text-black/70"
            @click="open = true"
          >
            <a href="#home-section">Home</a>
          </p>
          <p
            class="px-2 cursor-pointer hover:text-black/70"
            @click="open = true"
          >
            <a href="#skills-section">Skills</a>
          </p>
          <p
            class="px-2 cursor-pointer hover:text-black/70"
            @click="open = true"
          >
            <a href="#experience-section">Experience</a>
          </p>
          <p
            class="px-2 cursor-pointer hover:text-black/70"
            @click="open = true"
          >
            <a href="#projects-section">Projects</a>
          </p>

          <p
            class="px-4 py-1 rounded-md border-[#164085] text-[#164085] border-solid border-2 cursor-pointer"
          >
            Hire Me
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      open: true,
    };
  },
};
</script>
