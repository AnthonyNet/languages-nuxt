<template>
    <div
    class="snap-x z-10  fixed left-0 top-0 w-full h-screen bg-black/70">
    <div
      class="responsiveMenu fixed left-0 top-0 w-[85%] sm:w-[60%] md:w-[45%] h-screen mobile__Nav p-4 sm:p-8 ease-in duration-500"
    >
      <div class="flex justify-between items-center">
        <aside class="logo sm:mr-40">
          <NuxtLink href="/">
            Learn <strong>languages</strong>
          </NuxtLink>
        </aside>
        <div
          onClick={handleNav}
          class="navClose rounded-full shadow-lg shadow-gray-400 p-3 cursor-pointer"
        >
          Close
        </div>
      </div>
      <div class="mottoCover border-b border-gray-300 my-4 text-sm sm:text-lg">
        <p>Evolution means everyday learning</p>
      </div>
      <nav>
        <ul class="flex flex-col  z-20">
          <div class="flex justify-between items-center">
            <NuxtLink class="py-4 uppercase" href="/">
              Home
            </NuxtLink>
            <span class="bottom-2 right-4 text-3xl">
              DARK
            </span>
          </div>

          <main>
            <details class="py-4 cursor-pointer">
              <summary class="uppercase border-gray-300 border-b logo">
                <strong>English</strong>
              </summary>
              <ul class="flex flex-col navDetails">
                <NuxtLink to="/english/irregular-verbs">Irregular Verbs ({{IrregularVerbs.length}})</NuxtLink>
                <NuxtLink to="/english/search-irregular">Phrasal verbs ({{LukesPhrasal.length}})</NuxtLink>
                <NuxtLink to="/english/oxford-B1">Oxford B1 ({{OxfordB1.length}})</NuxtLink>
                <NuxtLink to="/english/oxford-B2">Oxford B2 ({{OxfordB1.length}})</NuxtLink>
                <NuxtLink to="/english/oxford-C1">OxfordB2 ({{OxfordB2.length}})</NuxtLink>
                <NuxtLink to="/english/phrasal-verbs">Oxford C1 ({{OxfordC1.length}})</NuxtLink>
                <NuxtLink to="/english/pagination">Pagination</NuxtLink>
              </ul>
            </details>

            <details class="cursor-pointer">
              <summary class="uppercase border-gray-300 border-b logo">
                <strong> Deutsch</strong>
              </summary>
              <ul class="flex flex-col navDetails">
                <NuxtLink to="/german/german">Irregular Verbs ({{VerbenData.length}})</NuxtLink>
                <NuxtLink to="/german/goethe">Goethe ({{Goethe.length}}) </NuxtLink>
              </ul>
            </details>
          </main>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
import IrregularVerbs from '../../myData/IrregularVerbs.js';
import LukesPhrasal from '../../myData/LukesPhrasal.js';
import OxfordB1 from '../../myData/OxfordB1.js';
import OxfordB2 from '../../myData/OxfordB2.js';
import OxfordC1 from '../../myData/OxfordC1.js';
import VerbenData from '../../myData/VerbenData.js';
import Goethe from '../../myData/Goethe.js';

  export default {
  name: 'MobileNav',
  data() {
    return {
      IrregularVerbs,
      LukesPhrasal,
      OxfordB1,
      OxfordB2,
      OxfordC1,
      VerbenData,
      Goethe,
    };
  },
};

const nav = true;

</script>

<style lang="scss" scoped>

</style>