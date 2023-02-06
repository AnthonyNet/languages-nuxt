<script>
      const styles = {
  section:
    "responsiveSection flex flex-col justify-center items-center w-full min-h-[88vh] h-auto sm:h-[90%] border-red-300  border-t-2",
  card__div:
    "mainCard w-[300px] h-[420px] cursor-pointer group perspective bg-gray-100",
  card__div__div:
    "preserve-3d group-hover:my-rotate-y-180  w-full h-full duration-1000",
  card__div__div__div: "w-full h-full",
  cardBack:
    "my-rotate-y-180 backface-hidden w-full h-full mt-[-420px] overflow-hidden shadow-lg shadow-gray-400 bg-gray-100",
  cardBack__div:
    "flex flex-col w-full  h-full  text-gray-800 px-2 pb-24",
  cardBack__div__btn:
    "bg-teal-500 px-6 py-2 mb-8 font-semibold text-white rounded-full delay-500 duration-1000 scale-0 group-hover:scale-125 ",
  button:
    "bg-teal-500 px-6 py-2 mb-auto mb-8 font-semibold text-white rounded-full delay-500 duration-1000 scale-0 group-hover:scale-125",
};

export default {
    props: ['title'],
  data() {
    return {
      styles,
    };
  },
};
</script>

<template>
    <section :class="[styles.section]">
        <div :class="[styles.card__div]">
          <div :class="[styles.card__div__div]">
            <div :class="[styles.card__div__div__div]">
            <h2 class="text-center">{{title}}</h2>
            </div>
            <div :class="[styles.cardBack]">
              <div :class="[styles.cardBack__div]">
                <h2 class="my-4 text-3xl font-semibold self-center">
            Česky
                </h2>
                <button :class="[styles.button]">Překlad</button>
              </div>
            </div>
          </div>
        </div>
      </section>
</template>



<style  scoped>

</style>