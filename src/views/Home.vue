<template>
  <div>
    <Intro />
    <About />
    <Skills />
    <GoToTopFAB />
  </div>
</template>

<script>
import Intro from "@/components/Intro";
import About from "@/components/About";
import Skills from "@/components/Skills";
import GoToTopFAB from "@/components/GoToTopFAB";

export default {
  components: {
    Intro,
    About,
    Skills,
    GoToTopFAB
  }
};
</script>
