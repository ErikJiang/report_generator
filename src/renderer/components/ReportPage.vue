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



    <v-table
        :width="1400"
        :height="500"
        :columns="columns"
        :table-data="tableData"
        even-bg-color="#f4f4f4"
        row-hover-color="#eee"
        row-click-color="#edf7ff"
        :cell-merge="cellMerge"
    ></v-table>

    <button class="alt" @click="backHome()">返回首页</button>
  </div>
</template>

<script>
import Vue from 'vue';

export default {
  name: "report-page",
  data() {
      return {
        tableData: [
            {"name":"赵伟","gender":"男","birthday":'1963-7-9',"height":"183","email":"zhao@gmail.com","tel":"156*****1987","hobby":"钢琴、书法、唱歌","address":"上海市黄浦区金陵东路569号17楼"},
            {"name":"李伟","gender":"男","birthday":'2003-12-7',"height":"166","email":"li@gmail.com","tel":"182*****1538","hobby":"钢琴、书法、唱歌","address":"上海市奉贤区南桥镇立新路12号2楼"},
            {"name":"孙伟","gender":"女","birthday":'1993-12-7',"height":"186","email":"sun@gmail.com","tel":"161*****0097","hobby":"钢琴、书法、唱歌","address":"上海市崇明县城桥镇八一路739号"},
            {"name":"周伟","gender":"女","birthday":'1993-12-7',"height":"188","email":"zhou@gmail.com","tel":"197*****1123","hobby":"钢琴、书法、唱歌","address":"上海市青浦区青浦镇章浜路24号"},
            {"name":"吴伟","gender":"男","birthday":'1993-12-7',"height":"160","email":"wu@gmail.com","tel":"183*****6678","hobby":"钢琴、书法、唱歌","address":"上海市松江区乐都西路867-871号"},
            {"name":"冯伟","gender":"女","birthday":'1993-12-7',"height":"168","email":"feng@gmail.com","tel":"133*****3793","hobby":"钢琴、书法、唱歌","address":"上海市金山区龙胜路143号一层"},
            {"name":"褚伟","gender":"男","birthday":'1993-12-7',"height":"170","email":"zhu@gmail.com","tel":"189*****2345","hobby":"钢琴、书法、唱歌","address":"上海市闵行区都市路2988号2楼"}
        ],
        columns: [
            {field: 'name', title:'姓名', width: 150, titleAlign: 'center',columnAlign:'center', isFrozen: true},
            {field: 'gender', title:'性别', width: 150, titleAlign: 'center',columnAlign:'center', isFrozen: true},
            {field: 'tel', title: '手机号码', width: 180, titleAlign: 'center',columnAlign:'center', isFrozen: false},
            {field: 'birthday', title: '出生日期', width: 180, titleAlign: 'center',columnAlign:'center'},
            {field: 'hobby', title: '爱好', width: 380, titleAlign: 'center',columnAlign:'center'},
            {field: 'address', title: '地址', width: 430, titleAlign: 'center',columnAlign:'left'}
        ]
      };
    
  },
  components: {},
  methods: {
    cellMerge(rowIndex,rowData,field){
        if (field === 'name' && rowData[field] === '李伟') {
            return {
                colSpan: 2,
                rowSpan: 1,
                content: '<span style="color:red">单元格 colSpan</span>',
                componentName: ''
            }
        } else if (rowIndex === 3 && field === 'gender') {
            return {
                colSpan: 1,
                rowSpan: 3,
                content: '<span style="color:red">单元格 rowSpan</span>',
                componentName: ''
            };
        }else if (rowIndex === 2 && field === 'birthday') {
            return {
                colSpan: 2,
                rowSpan: 3,
                content:'',
                componentName:'table-cell-merge',
            }
        }
    },
    backHome() {
      this.$router.push("/");
    }
  }
};

Vue.component('table-cell-merge',{
    template:`<span style="color:red">
        单元格 rowSpan 和 colSpan 同时使用
        </span>`,
    props:{
        rowData:{
            type:Object
        },
        field:{
            type:String
        },
        index:{
            type:Number
        }
    }
});
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
