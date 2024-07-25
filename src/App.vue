<script setup>
import { ref } from 'vue'

import MyComponent from './components/MyComponent.vue'
import GlobalStyle from './components/GlobalStyle.vue'
import LocalStyle from './components/LocalStyle.vue'
import CombinedStyle from './components/CombinedStyle.vue'
import ModuleStyle from './components/ModuleStyle.vue'
import MyEvent from './components/MyEvent.vue'
import MyReactiveComponent from './components/MyReactiveComponent.vue'
import MyRefComponent from './components/MyRefComponent.vue'
import ConditionalRendering from './components/ConditionalRendering.vue'
import ComputedProperties from './components/ComputedProperties.vue'
import IterationComponent from './components/IterationComponent.vue'
import StaticPropsComponent from './components/StaticPropsComponent.vue'
import DynamicPropsComponent from './components/DynamicPropsComponent.vue'
import ChangingPropsValue from './components/ChangingPropsValue.vue'
import PropValidation from './components/PropValidation.vue'
import ComplexProps from './components/ComplexProps.vue'
import CustomValidator from './components/CustomValidator.vue'
import ComponentEvent from './components/ComponentEvent.vue'

const firstName = ref('HuXn')
const lastName = ref('WebDEv')
const myFavouriteNumber = ref(5)
let count = ref(0)
</script>
<template>
  <MyComponent />
  <GlobalStyle />
  <LocalStyle />
  <CombinedStyle />
  <ModuleStyle />
  <MyEvent />
  <MyReactiveComponent />
  <MyRefComponent />
  <ConditionalRendering />
  <ComputedProperties />
  <IterationComponent />
  <StaticPropsComponent name="Ria" />
  <DynamicPropsComponent :firstName="firstName" :lastName="lastName" />
  <ChangingPropsValue :myFavouriteNumber="myFavouriteNumber" />
  <PropValidation fullName="Ria" :age="22" />
  <ComplexProps
    :friends="['alex', 'john', 'jordan', 'Ria']"
    :userInfo="{ name: 'alex', age: 22, location: ['Earth', 'IDK'] }"
  />
  <hr />
  <CustomValidator name="Ria" :age="20" password="impossiblePassword" />

  <h1>Count: {{ count }}</h1>
  <ComponentEvent @incrementCounter="count++" />
</template>
<style scoped></style>
