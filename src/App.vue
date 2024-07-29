<script setup>
import { ref } from 'vue'
import { provide } from 'vue'

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
import FormComponent from './components/FormComponent.vue'
import SlotComponent from './components/SlotComponent.vue'
import FallbackContent from './components/FallbackContent.vue'
import NamedSlot from './components/NamedSlot.vue'
import DefaultSlot from './components/DefaultSlot.vue'
import SchoolComponent from './components/SchoolComponent.vue'
import PracticeComponent from './components/PracticeComponent.vue'
import LifeCycleComponent from './components/LifeCycleComponent.vue'
import BasicComponent from './components/BasicComponent.vue'
import ReactiveObject from './components/ReactiveObject.vue'
import MultipleSources from './components/MultipleSources.vue'
import BasicRef from './components/BasicRef.vue'
import FunctionRef from './components/FunctionRef.vue'
import RefComponents from './components/RefComponents.vue'
import ToggleFriends from './components/ToggleFriends.vue'
import CounterComponent from './components/CounterComponent.vue'
import MineComponent from './components/MineComponent.vue'
import MainComponent from './components/MainComponent.vue'
import GettingDataWithFetch from './components/GettingDataWithFetch.vue'
import GettingDataWithAxios from './components/GettingDataWithAxios.vue'
import TodoList from './components/TodoList.vue'

const firstName = ref('HuXn')
const lastName = ref('WebDEv')
const myFavouriteNumber = ref(5)
let count = ref(0)

const formHandler = (username, email, password) => {
  console.log('username: ', username)
  console.log('email: ', email)
  console.log('password: ', password)
}

const studentName = 'alex'
const studentAge = 20
const studentLocation = ['Earth', 'IDK']

provide('studentName2', 'Gloria')
provide('studentAge2', 22)
provide('studentLocation2', ['Earth', 'IDK'])

//provide Array
provide('friends', ['Alex', 'Jordan', 'Ria', 'John'])

//provide Object
provide('games', {
  id: 1,
  title: 'Epic Adventure Game',
  genre: ['Action', 'Adventure', 'RPG'],
  platform: ['PC', 'PlayStation', 'Xbox', 'Nintendo Switch'],
  realeaseDate: '2023-03-15',
  developer: {
    name: 'Awesome Game Studios',
    location: 'San Fracisco, CA',
    teamSize: 50
  }
})

//Provide Array of Objects
provide('moreGames', [
  {
    title: 'Space Explorer',
    genre: 'Sci-Fi',
    platform: 'PC',
    realeaseDate: '2023-05-20'
  },
  {
    title: 'Fantasy Quest',
    genre: 'Fantasy',
    platform: 'PlayStation',
    realeaseDate: '2023-07-10'
  },
  {
    title: 'Inception',
    director: 'Christopher Nolan',
    genre: 'Sci-Fi',
    realeaseDate: '2010-07-16'
  },
  {
    title: 'The Shawshank Redemption',
    director: 'Frank Darabont',
    genre: 'Drama',
    realeaseDate: '1994-09-23'
  }
])

const showHide = ref(true)
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

  <FormComponent @userInfo="formHandler" />

  <SlotComponent>
    <h1>Content one</h1>
    <h2>Content two</h2>
  </SlotComponent>

  <FallbackContent></FallbackContent>

  <hr />

  <NamedSlot>
    <!-- v-slot:one  -->
    <template v-slot:one>
      <h1>This content will go to slot 'one'</h1>
    </template>

    <!-- #two -->
    <template #two>
      <h1>This content will go to slot 'two'</h1>
    </template>
  </NamedSlot>
  <DefaultSlot>
    <template>
      <h1>This is some random default content</h1>
    </template>
  </DefaultSlot>

  <!-- <SchoolComponent
    :studentName="studentName"
    :studentAge="studentAge"
    :studentLocation="studentLocation"
  /> -->

  <SchoolComponent />
  <hr />
  <PracticeComponent />
  <hr />
  <LifeCycleComponent v-if="showHide" />
  <hr />
  <button @click="showHide = !showHide">Show / Hide</button>
  <hr />
  <BasicComponent />
  <hr />
  <ReactiveObject />
  <hr />
  <MultipleSources />
  <hr />
  <BasicRef />
  <hr />
  <FunctionRef />
  <hr />
  <RefComponents />
  <hr />
  <ToggleFriends />
  <hr />
  <CounterComponent />
  <hr />
  <MineComponent />
  <hr />
  <MainComponent />
  <hr />
  <GettingDataWithFetch />
  <hr />
  <GettingDataWithAxios />
  <hr />
  <TodoList />
</template>
<style scoped></style>
