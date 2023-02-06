<script>
import Navbar from "~/components/navbar/Navbar.vue";
import Irregular from "~/components/irregular/Irregular.vue";
const styles = {
  section:
    "section_Responsive flex justify-center items-center w-full h-[91vh] responsiveSection border",
  section_div:
    "max-w-sm card my-8 xl:my-0 border-4 border-double border-blue-700 rounded-lg shadow-xl shadow-slate-600 text-center",
  score_div: "py-3 px-6 border-b border-gray-300",
  btn_div: "border-t border-gray-300 text-gray-600",
  h5: "text-xl dark:bg-black font-medium mb-2 border-b border-gray-300",
  ul: "flex flex-col justify-around text-center mb-2",
};
export default {
  components: {
    Navbar,
    Irregular,
  },
  data(){
    return{
      styles
    };
  },
};
</script>

<template>
  <section className="{styles.section}">
    <div className="{styles.section_div}">
      <div className="{styles.score_div}">Celkové skóre: <span>0</span></div>
      <div className="{styles.score_div}">Momentální skóre: <span>0</span></div>

      <p>Score</p>

      <div className="px-6 inputs">
        <h5 className="{styles.h5}">cz</h5>

        <ul className="{styles.ul}">
          <li>
            <Irregular />
          </li>
        </ul>
      </div>
    </div>
  </section>
  
</template>

<style lang="sass" scoped></style>
