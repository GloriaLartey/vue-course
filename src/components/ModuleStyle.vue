<template>
  <h1 :class="myClasses['m-class']">Using Module CSS with $ syntax (kebab-case)</h1>
  <h1 :class="myClasses.anotherclass">Using CSS with $ syntax(camelCase)</h1>
</template>

<style module="myClasses">
/* Kebab-case */
.m-class {
  background-color: firebrick;
  color: white;
}

.anotherclass {
  background-color: seagreen;
  color: white;
}
</style>
