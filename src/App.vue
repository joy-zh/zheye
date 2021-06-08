<template>
  <div class="container">
    <global-header :user="currentUser"></global-header>
    <column-list :list="list"></column-list>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import 'bootstrap/dist/css/bootstrap.min.css'
import ColumnList, { ColumnProps } from './components/ColumnList.vue'
import GlobalHeader, { UserProps } from './components/GlobalHeader.vue'

const currentUser: UserProps = {
  isLogin: true,
  name: '于谦',
  id: 12
}

const testData: ColumnProps[] = [
  {
    id: 1,
    title: 'test1的标题',
    description: 'test1的描述：理科生居第二位，深刻的垃圾分类',
    avatar: 'https://img0.baidu.com/it/u=1531038383,3455172191&fm=26&fmt=auto&gp=0.jpg'
  },
  {
    id: 2,
    title: 'test2的标题',
    description: 'test2的描述：理科生居第二位，死了都快使点劲',
    avatar: 'https://img2.baidu.com/it/u=2306696130,3636777462&fm=26&fmt=auto&gp=0.jpg'
  },
  {
    id: 3,
    title: 'test2的标题',
    description: 'test2的描述：理科生居第二位，死了都快使点劲'
  },
  {
    id: 4,
    title: 'test2的标题',
    description: 'test2的描述：理科生居第二位，死了都快使点劲',
    avatar: 'https://img2.baidu.com/it/u=2306696130,3636777462&fm=26&fmt=auto&gp=0.jpg'
  }
]

export default defineComponent({
  name: 'App',
  components: {
    ColumnList,
    GlobalHeader
  },
  setup () {
    return {
      list: testData,
      currentUser
    }
  }
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
