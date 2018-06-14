<template>
  <div id="wrapper">
    <h1>检验报告</h1>
    <p>No.2018(浦东机场)-03-1</p>
    <p>样品名称：<u>后扩底锚栓KUA22×100 M16/80</u></p>
    <p>委托单位：<u>中铁四局上海浦东机场三期扩建工程捷运系统铺轨、供电及接触轨、通信、信号、系统项目经理部</u></p>
    <p>生产单位：<u>上海康驰建筑技术有限公司</u></p>
    <p>检验类别：<u>抽查检验</u></p>

    <h3>中铁宝鸡轨道电气设备检测有限公司</h3>
    <h5>China Railway Baoji Rail Transit Electrical Equipment Test Co.，Ltd.</h5>
    
    <br>
    <hr>
    <br>

    <h3>声 明</h3>
    <p>1. 检验报告无公司封印和检测报告专用章无效。</p>
    <p>2. 未经本公司书面批准，不得复制报告，复制报告未重新加盖本中心封印和检测报告专用章无效。</p>
    <p>3. 检验报告无编写、审核、批准人签字无效。</p>
    <p>4. 检验报告涂改无效。</p>
    <p>5. 一般情况，委托检验仅对样品负责。</p>
    <p>6. 用户若对检验结果有异议，请于收到报告之日起十五日内向本中心提出。</p>
    <br>
    <p>通讯地址：</p>
    <p>中国陕西省宝鸡市东风路59号</p>
    <p>邮编：721000</p>
    <p>电话：（0917） 3832699、3832689、2829830</p>
    <p>路电：（017）29830、32699</p>
    <p>传真：0917-3832689</p>

    <br>
    <hr>
    <br>

    <table>
      <tr v-for="user in data">
        <td class="text center" v-text="user.name" @dblclick="editable($event,'name',user)"></td>
        <td class="text center" v-text="user.name" @dblclick="editable($event,'name',user)"></td>
      </tr>
    </table>


    <button class="alt" @click="backHome()">返回首页</button>
  </div>
</template>

<script>
export default {
  name: "report-page",
  data() {
    return {
      data: [{ name: "123" }, { name: "4451" }]
    };
  },
  components: {},
  methods: {
    editable: function(e, field, user) {
      let that = this;
      that.$editable(e, function(value) {});
    },
    backHome() {
      this.$router.push("/");
    }
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Source+Sans+Pro");

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: "Source Sans Pro", sans-serif;
}

#wrapper {
  background: radial-gradient(
    ellipse at top left,
    rgba(255, 255, 255, 1) 40%,
    rgba(229, 229, 229, 0.9) 100%
  );
  height: 100vh;
  padding: 60px 80px;
  width: 100vw;
}
</style>
