<template>
  <div>
    <div>
      这里是测试页面一
    </div>
    接口返回数据：{{posts}}
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData({$axios}){
    const result = await $axios.get('http://localhost:8000/post')
    return{
      posts: result.data
    }
  }
}
</script>
