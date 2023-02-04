<script>
import IrregularVerbs from '../../myData/IrregularVerbs.js';
import LukesPhrasal from '../../myData/LukesPhrasal.js';
import OxfordB1 from '../../myData/OxfordB1.js';
import OxfordB2 from '../../myData/OxfordB2.js';
import OxfordC1 from '../../myData/OxfordC1.js';
import VerbenData from '../../myData/VerbenData.js';
import Goethe from '../../myData/Goethe.js';

const styles = {
  nav: 'flex justify-center items-center w-full  min-h-[100px] shadow-xl z-[400] px-4',
  nav__div: 'navDetails w-full h-full flex items-start  relative text-xl ',
  aside: 'logo sm:w-1/3 ',
  article: 'justify-around items-start w-full h-full hidden md:flex',
  nav__ul: 'flex flex-col border-solid border-t-4 border-sky-400 navDetails',
}

export default {
  name: 'Navbar',
  data() {
    return {
      styles,
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

</script>

<template>
    <nav
    class={styles.nav}
   
  >
    <div class={styles.nav__div}>
      <aside className={styles.aside}>
        <NuxtLink to="/">
          Learn <strong>languages</strong>
        </NuxtLink>
      </aside>
      <article className={styles.article}>
        <NuxtLink to="/">Home</NuxtLink>
        <details class="cursor-pointer">
          <summary class="uppercase logo">
            <strong class="hover:text-sky-700">English</strong>
          </summary>
          <div className={styles.nav__ul}>
            <NuxtLink to="/english/irregular-verbs">Irregular Verbs ({{IrregularVerbs.length}})</NuxtLink>
            <NuxtLink to="/english/search-irregular">Irregular List ({{IrregularVerbs.length}})</NuxtLink>
            <NuxtLink to="/english/oxford-B1">Oxford B1 ({{OxfordB1.length}})</NuxtLink>
            <NuxtLink to="/english/oxford-B2">Oxford B2 ({{OxfordB2.length}})</NuxtLink>
            <NuxtLink to="/english/oxford-C1">Oxford C1 ({{OxfordC1.length}})</NuxtLink>
            <NuxtLink to="/english/phrasal-verbs">Phrasal Verbs ({{LukesPhrasal.length}})</NuxtLink>
            <NuxtLink to="/english/pagination">Pagination</NuxtLink>
          </div>
        </details>

        <details class="cursor-pointer">
          <summary class="uppercase logo">
            <strong class="hover:text-sky-700">Deutsch</strong>
          </summary>
          <ul class="flex flex-col border-solid border-t-4 border-sky-400 navDetails">
            <NuxtLink to="/german/irregular-verbs">Irregular Verbs ({{ VerbenData.length }})</NuxtLink>
            <NuxtLink to="/german/goethe">Göethe ({{ Goethe.length }})</NuxtLink>
          </ul>
        </details>
      </article>

      <span class="hidden md:flex  bottom-2 right-4 text-3xl">
        dark
      </span>

      <div class="text-4xl md:hidden ml-auto">
        <p>menu</p>
      </div>
    </div>

   <p>nav</p>
  </nav>

</template>



<style lang="scss" scoped>

</style>