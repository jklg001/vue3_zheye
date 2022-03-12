<template>
  <div class="container">
    <global-header :user="testUser"></global-header>
    <ColumnList :list = "testData"/>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import ColumnList, { ColumnProps } from './components/ColumnList.vue'
import GlobalHeader, { UserProps } from './components/GlobalHeader.vue'
import 'bootstrap/dist/css/bootstrap.min.css'
const testData: ColumnProps[] = [
  {
    id: 1,
    title: 'test1的专栏',
    description: '这是的test1专栏,有一段非常有意思的简介,可以更新一下欧',
    avatar: 'http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5f3e41a8b7d9c60b68cdd1ec.jpg?x-oss-process=image/resize,m_pad,h_50,w_50'
  },
  {
    id: 2,
    title: 'test2的专栏',
    description: '这是的test2专栏,有一段非常有意思的简介,可以更新一下欧',
    avatar: ''
  },
  {
    id: 3,
    title: 'test3的专栏',
    description: '这是的test3专栏,有一段非常有意思的简介,可以更新一下欧',
    avatar: 'http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5f3e41a8b7d9c60b68cdd1ec.jpg?x-oss-process=image/resize,m_pad,h_50,w_50'
  },
  {
    id: 4,
    title: 'test4的专栏',
    description: '这是的test4专栏,有一段非常有意思的简介,可以更新一下欧',
    avatar: 'http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5f3e41a8b7d9c60b68cdd1ec.jpg?x-oss-process=image/resize,m_pad,h_50,w_50'
  }
]
const testUser: UserProps = {
  isLogin: false,
  name: '种太阳',
  id: 3
}
export default defineComponent({
  name: 'App',
  components: {
    ColumnList,
    GlobalHeader
  },
  setup () {
    return {
      testData,
      testUser
    }
  }
})
</script>

<style>
</style>
