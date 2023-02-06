<script>
   import Input from "~/components/irregular/Input.vue";

const styles = {
  section: "dick flex justify-center items-center w-full h-[91vh] bg-orange-200",
  section_div: "max-w-sm card my-8 xl:my-0 border-4 border-double border-blue-700 rounded-lg shadow-xl shadow-slate-600 text-center",
  score_div: "py-3 px-6 border-b border-gray-300",
  btn_div: "border-t border-gray-300 text-gray-600",
  h5: "text-xl dark:bg-black font-medium mb-2 border-b border-gray-300",
  ul: "flex flex-col justify-around text-center mb-2",
};
export default {

  components: {
    Input,
  },
  data(){
    return{
      styles,
      dataX: 'přepisování',
   
    };
  },
};

</script>

<template>
    <section :class="[styles.section]">
      <div :class="[styles.section_div]">
        <div :class="[styles.score_div]">Celkové skóre: <span>0</span></div>
        <div :class="[styles.score_div]">Momentální skóre: <span>0</span></div>
  
        <p>Score</p>
  
        <div class="px-6 inputs">
          <h5 :class="[styles.h5]">cz</h5>
  
          <ul :class="[styles.ul]">
              <li>{{dataX}}</li>
            <li>
              <Input   @udalost="dataX = $event"/>
            </li>
          </ul>
        </div>
      </div> 
    </section>
    
</template>



<style scoped>

</style>