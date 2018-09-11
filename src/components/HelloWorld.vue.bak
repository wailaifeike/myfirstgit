<template>
<div>
  <el-row><h3>单词翻译</h3></el-row>
  <el-row>
    <el-col :span="5" :offset="8"><el-input placeholder="请输入内容" v-model="input10" clearable></el-input>

    </el-col>

    <div style="float: left">
            <el-select v-model="value4" clearable placeholder="请选择">
            <el-option v-for="item in options" :key="item.value" :label="item.label" :value="item.value"></el-option>
            </el-select>
    </div>
    <div style="float: left"><el-button  icon="el-icon-search" circle @click="handlebtn"></el-button></div>
  </el-row><el-row><el-col :span="5" :offset="10"><el-input type="textarea" :rows="2" placeholder="翻译后的内容" v-model="textarea"></el-input></el-col></el-row>


</div>

</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      input10: '',
      input11:'',
      textarea:"",
      options: [{
        value: 'en',
        label: 'English'
      }, {
        value: 'zh',
        label: 'Chinese'
      }, {
        value: 'ko',
        label: 'Korean'
      }, {
        value: 'mg',
        label: 'Japanese'
      }, {
        value: 'ru',
        label: 'Russian'
      },
        {
          value: 'es',
          label: 'Spanish'
        }],
      value4: '',
      value11: [],

    }
  },
  methods:{
    handlebtn(){

      console.log(this.url+this.input10)
     this.$http.get( "https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20180826T122615Z.26e8727a095f940c.3d5225ecf3d398933b8458bc600459a8ce2fedd9&lang="+this.value4+"&text="+this.input10).then(function (res) {
       this.textarea = res.body.text[0]
     },function (res) {
       console.log(res)
       alert("请求失败！")
       }
     )
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
