<script setup lang="ts">
defineProps<{
  flex?: boolean;
  grow?: boolean;
  noGrow?: boolean;
  shrink?: boolean;
  noShrink?: boolean;
  sm?: boolean;
  md?: boolean;
  lg?: boolean;
  xl?: boolean;
  txl?: boolean;
  hidden?: boolean;
  smHidden?: boolean;
  mdHidden?: boolean;
  lgHidden?: boolean;
  xlHidden?: boolean;
  txlHidden?: boolean;
  row?: boolean;
  smRow?: boolean;
  mdRow?: boolean;
  lgRow?: boolean;
  xlRow?: boolean;
  txlRow?: boolean;
  column?: boolean;
  smColumn?: boolean;
  mdColumn?: boolean;
  lgColumn?: boolean;
  xlColumn?: boolean;
  txlColumn?: boolean;
  wrap?: boolean;
  router?: boolean;
  to?: string;
  is?: string;
  items?: "start" | "center" | "end";
  smItems?: "start" | "center" | "end";
  mdItems?: "start" | "center" | "end";
  lgItems?: "start" | "center" | "end";
  xlItems?: "start" | "center" | "end";
  txlItems?: "start" | "center" | "end";
  justify?: "start" | "center" | "end" | "between" | "around" | "evenly";
  smJustify?: "start" | "center" | "end" | "between" | "around" | "evenly";
  mdJustify?: "start" | "center" | "end" | "between" | "around" | "evenly";
  lgJustify?: "start" | "center" | "end" | "between" | "around" | "evenly";
  xlJustify?: "start" | "center" | "end" | "between" | "around" | "evenly";
  txlJustify?: "start" | "center" | "end" | "between" | "around" | "evenly";
}>();
</script>

<template>
  <NuxtLink
      v-if="router"
      :to="to"
      :class="{
            flex: !hidden,
            'sm:flex': sm,
            'md:flex': md,
            'lg:flex': lg,
            'xl:flex': xl,
            'txl:flex': txl,
            hidden: hidden,
            'sm:hidden': smHidden,
            'md:hidden': mdHidden,
            'lg:hidden': lgHidden,
            'xl:hidden': xlHidden,
            'txl:hidden': txlHidden,
            'flex-row': row,
            'sm:flex-row': smRow,
            'md:flex-row': mdRow,
            'lg:flex-row': lgRow,
            'xl:flex-row': xlRow,
            '2xl:flex-row': txlRow,
            'flex-col': column,
            'sm:flex-col': smColumn,
            'md:flex-col': mdColumn,
            'lg:flex-col': lgColumn,
            'xl:flex-col': xlColumn,
            '2xl:flex-col': txlColumn,
            'flex-wrap': wrap,
            'justify-start': justify === 'start',
            'justify-center': justify === 'center',
            'justify-end': justify === 'end',
            'justify-between': justify === 'between',
            'justify-around': justify === 'around',
            'justify-evenly': justify === 'evenly',
            'sm:justify-start': smJustify === 'start',
            'sm:justify-center': smJustify === 'center',
            'sm:justify-end': smJustify === 'end',
            'sm:justify-between': smJustify === 'between',
            'sm:justify-around': smJustify === 'around',
            'sm:justify-evenly': smJustify === 'evenly',
            'md:justify-start': mdJustify === 'start',
            'md:justify-center': mdJustify === 'center',
            'md:justify-end': mdJustify === 'end',
            'md:justify-between': mdJustify === 'between',
            'md:justify-around': mdJustify === 'around',
            'md:justify-evenly': mdJustify === 'evenly',
            'lg:justify-start': lgJustify === 'start',
            'lg:justify-center': lgJustify === 'center',
            'lg:justify-end': lgJustify === 'end',
            'lg:justify-between': lgJustify === 'between',
            'lg:justify-around': lgJustify === 'around',
            'lg:justify-evenly': lgJustify === 'evenly',
            'xl:justify-start': xlJustify === 'start',
            'xl:justify-center': xlJustify === 'center',
            'xl:justify-end': xlJustify === 'end',
            'xl:justify-between': xlJustify === 'between',
            'xl:justify-around': xlJustify === 'around',
            'xl:justify-evenly': xlJustify === 'evenly',
            '2xl:justify-start': txlJustify === 'start',
            '2xl:justify-center': txlJustify === 'center',
            '2xl:justify-end': txlJustify === 'end',
            '2xl:justify-between': txlJustify === 'between',
            '2xl:justify-around': txlJustify === 'around',
            '2xl:justify-evenly': txlJustify === 'evenly',
            'items-start': items === 'start',
            'items-center': items === 'center',
            'items-end': items === 'end',
            'sm:items-start': smItems === 'start',
            'sm:items-center': smItems === 'center',
            'sm:items-end': smItems === 'end',
            'md:items-start': mdItems === 'start',
            'md:items-center': mdItems === 'center',
            'md:items-end': mdItems === 'end',
            'lg:items-start': lgItems === 'start',
            'lg:items-center': lgItems === 'center',
            'lg:items-end': lgItems === 'end',
            'xl:items-start': xlItems === 'start',
            'xl:items-center': xlItems === 'center',
            'xl:items-end': xlItems === 'end',
            '2xl:items-start': txlItems === 'start',
            '2xl:items-center': txlItems === 'center',
            '2xl:items-end': txlItems === 'end',
            'flex-1': flex,
            'flex-grow': grow,
            'flex-grow-0': noGrow,
            'flex-shrink': shrink,
            'flex-shrink-0': noShrink,
        }"
  >
    <slot />
  </NuxtLink>
  <Component
      v-else
      :is="is ? is : 'div'"
      :class="{
            flex: !hidden,
            'sm:flex': sm,
            'md:flex': md,
            'lg:flex': lg,
            'xl:flex': xl,
            'txl:flex': txl,
            hidden: hidden,
            'sm:hidden': smHidden,
            'md:hidden': mdHidden,
            'lg:hidden': lgHidden,
            'xl:hidden': xlHidden,
            'txl:hidden': txlHidden,
            'flex-row': row,
            'sm:flex-row': smRow,
            'md:flex-row': mdRow,
            'lg:flex-row': lgRow,
            'xl:flex-row': xlRow,
            '2xl:flex-row': txlRow,
            'flex-col': column,
            'sm:flex-col': smColumn,
            'md:flex-col': mdColumn,
            'lg:flex-col': lgColumn,
            'xl:flex-col': xlColumn,
            '2xl:flex-col': txlColumn,
            'flex-wrap': wrap,
            'justify-start': justify === 'start',
            'justify-center': justify === 'center',
            'justify-end': justify === 'end',
            'justify-between': justify === 'between',
            'justify-around': justify === 'around',
            'justify-evenly': justify === 'evenly',
            'sm:justify-start': smJustify === 'start',
            'sm:justify-center': smJustify === 'center',
            'sm:justify-end': smJustify === 'end',
            'sm:justify-between': smJustify === 'between',
            'sm:justify-around': smJustify === 'around',
            'sm:justify-evenly': smJustify === 'evenly',
            'md:justify-start': mdJustify === 'start',
            'md:justify-center': mdJustify === 'center',
            'md:justify-end': mdJustify === 'end',
            'md:justify-between': mdJustify === 'between',
            'md:justify-around': mdJustify === 'around',
            'md:justify-evenly': mdJustify === 'evenly',
            'lg:justify-start': lgJustify === 'start',
            'lg:justify-center': lgJustify === 'center',
            'lg:justify-end': lgJustify === 'end',
            'lg:justify-between': lgJustify === 'between',
            'lg:justify-around': lgJustify === 'around',
            'lg:justify-evenly': lgJustify === 'evenly',
            'xl:justify-start': xlJustify === 'start',
            'xl:justify-center': xlJustify === 'center',
            'xl:justify-end': xlJustify === 'end',
            'xl:justify-between': xlJustify === 'between',
            'xl:justify-around': xlJustify === 'around',
            'xl:justify-evenly': xlJustify === 'evenly',
            '2xl:justify-start': txlJustify === 'start',
            '2xl:justify-center': txlJustify === 'center',
            '2xl:justify-end': txlJustify === 'end',
            '2xl:justify-between': txlJustify === 'between',
            '2xl:justify-around': txlJustify === 'around',
            '2xl:justify-evenly': txlJustify === 'evenly',
            'items-start': items === 'start',
            'items-center': items === 'center',
            'items-end': items === 'end',
            'sm:items-start': smItems === 'start',
            'sm:items-center': smItems === 'center',
            'sm:items-end': smItems === 'end',
            'md:items-start': mdItems === 'start',
            'md:items-center': mdItems === 'center',
            'md:items-end': mdItems === 'end',
            'lg:items-start': lgItems === 'start',
            'lg:items-center': lgItems === 'center',
            'lg:items-end': lgItems === 'end',
            'xl:items-start': xlItems === 'start',
            'xl:items-center': xlItems === 'center',
            'xl:items-end': xlItems === 'end',
            '2xl:items-start': txlItems === 'start',
            '2xl:items-center': txlItems === 'center',
            '2xl:items-end': txlItems === 'end',
            'flex-1': flex,
            'flex-grow': grow,
            'flex-grow-0': noGrow,
            'flex-shrink': shrink,
            'flex-shrink-0': noShrink,
        }"
  >
    <slot />
  </Component>
</template>