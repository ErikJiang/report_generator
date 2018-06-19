<template>

  <el-container>
    <el-header>
      <el-menu class="menu" mode="horizontal">
        <el-menu-item index="1">
          <el-button round @click="backHome()"> 
          <i class='el-icon-back'></i> 返回首页
          </el-button>
        </el-menu-item>
        
        <el-menu-item index="2">
          <el-button round>
            <i class="el-icon-check"></i> 当前保存
          </el-button>
        </el-menu-item>
        <el-menu-item index="3">
          <el-button round @click="exportDocx()">
            <i class="el-icon-download"></i> 报告导出
          </el-button>
        </el-menu-item>
    </el-menu>
    </el-header>
    
    <el-main>
      <div id="wrapper">
        <div id="docxContent">
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
            <tbody>
              <tr>
                <td rowspan="2">中铁宝鸡轨道电气设备检测有限公司</td>
                <td rowspan="2"><h2>检验报告</h2></td>
                <td colspan="2">№.2018（浦东机场）-03-1</td>
              </tr>
              <tr>
                <td colspan="2">共2页  第1页</td>
              </tr>
              <tr>
                <td>工程名称</td>
                <td colspan="3" v-text="report1.projectName" @dblclick="editable($event)"></td>
              </tr>
              <tr>
                <td>委托单位</td>
                <td v-text="report1.entrustCo" @dblclick="editable($event)"></td>
                <td>联系人/电话</td>
                <td v-text="report1.entrustLink" @dblclick="editable($event)"></td>
              </tr>
              <tr>
                <td>联系地址</td>
                <td v-text="report1.entrustAddr" @dblclick="editable($event)"></td>
                <td>检验类别</td>
                <td v-text="report1.checkType" @dblclick="editable($event)"></td>
              </tr>
              <tr>
                <td>生产单位</td>
                <td v-text="report1.productCo" @dblclick="editable($event)"></td>
                <td>联系人/电话</td>
                <td v-text="report1.productLink" @dblclick="editable($event)"></td>
              </tr>
              <tr>
                <td rowspan="2">样品名称、型号规格、数量</td>
                <td rowspan="2">后扩底锚栓、KUA22×100 M16/80、9套</td>
                <td>样品标识</td>
                <td>/</td>
              </tr>
              <tr>
                <td>抽样人</td>
                <td>王展翔</td>
              </tr>
              <tr>
                <td rowspan="2">检验日期</td>
                <td rowspan="2">2018.6.11</td>
                <td>到样日期</td>
                <td>2018.5.19</td>
              </tr>
              <tr>
                <td>样品状态</td>
                <td>样品表面完好</td>
              </tr>
              <tr>
                <td>检验依据</td>
                <td colspan="3">DG/TJ08-003-2013《建筑锚栓抗拉拔、抗剪性能试验方法》及厂家力学性能及安装尺寸技术要求。</td>
              </tr>
              <tr>
                <td>检验项目</td>
                <td colspan="3">锚栓现场拉拔试验</td>
              </tr>
              <tr>
                <td>主要检测设备</td>
                <td colspan="3">锚栓拉拔仪 201006024</td>
              </tr>
              <tr>
                <td>检验结论</td>
                <td colspan="3">
                  <p>
                    经检验，受检产品检验项目达到技术要求，抽查检验合格。
                                              (检验报告专用章)
                                              签发日期 2018年6月12日
                  </p>
                </td>
              </tr>
              <tr>
                <td>编写</td>
                <td colspan="3">苗宇</td>
              </tr>
              <tr>
                <td>审核（机电）</td>
                <td colspan="3"></td>
              </tr>
              <tr>
                <td>批准（机电）</td>
                <td colspan="3"></td>
              </tr>
              <tr>
                <td>备  注</td>
                <td colspan="3"></td>
              </tr>
            </tbody>
            
          </table>

          <br>
          <hr>
          <br>

          <table>
            <tbody>
              <tr>
                <td rowspan="2" colspan="2">中铁宝鸡轨道电气设备检测有限公司</td>
                <td rowspan="2" colspan="6"><h2>检验报告</h2></td>
                <td rowspan="1" colspan="2">样品名称/型号规格</td>
                <td rowspan="1" colspan="3">№.2018（浦东机场）-03-1</td>
              </tr>
              <tr>
                <td rowspan="1" colspan="2">后扩底锚栓/KUA22×100 M16/80</td>
                <td rowspan="1" colspan="3">共2页 第2页</td>
              </tr>
              <tr>
                <td rowspan="2">序号</td>
                <td rowspan="2">检验项目</td>
                <td rowspan="2">技术要求</td>
                <td rowspan="2">单位</td>
                <td colspan="9">样品编号及检验结果</td>
              </tr>
              <tr>
                <td>10#</td>
                <td>11#</td>
                <td>12#</td>
                <td>13#</td>
                <td>14#</td>
                <td>15#</td>
                <td>16#</td>
                <td>17#</td>
                <td>18#</td>
              </tr>
              <tr>
                <td colspan="1">1</td>
                <td colspan="1">锚栓现场拉拔试验</td>
                <td colspan="1">设计载荷≥38.4kN</td>
                <td colspan="1">kN</td>
                <td colspan="1">39.1kN保荷2分钟载荷未降低</td>
                <td colspan="1">39.7kN保荷2分钟载荷未降低</td>
                <td colspan="1">39.6kN保荷2分钟载荷未降低</td>
                <td colspan="1">38.9kN保荷2分钟载荷未降低</td>
                <td colspan="1">39.9kN保荷2分钟载荷未降低</td>
                <td colspan="1">39.4kN保荷2分钟载荷未降低</td>
                <td colspan="1">38.6kN保荷2分钟载荷未降低</td>
                <td colspan="1">38.7kN保荷2分钟载荷未降低</td>
                <td colspan="1">39.1kN保荷2分钟载荷未降低</td>
              </tr>
              <tr>
                <td colspan="2">备注</td>
                <td colspan="11">/</td>
              </tr>
            </tbody>
          </table>

          <br>
          <hr>
          <br>
        </div>
      </div>
    </el-main>

  </el-container>  

</template>

<script>
export default {
  name: "report-page",
  data() {
    return {
      data: [{ name: "123" }, { name: "4451" }],
      report1: {
        projectName: "上海浦东国际机场旅客捷运系统工程",
        entrustCo:
          "中铁四局上海浦东机场三期扩建工程捷运系统铺轨、供电及接触轨、通信、信号、系统项目经理部",
        entrustLink: "何立峥 18656676477",
        entrustAddr: "上海市浦东新区祝桥镇围场河路",
        checkType: "抽查检验",
        productCo: "上海康驰建筑技术有限公司",
        productLink: "张鑫 18616303505"
      }
    };
  },
  components: {},
  methods: {
    editable: function(e) {
      let that = this;
      that.$editable(e, function(value) {});
    },
    backHome() {
      this.$router.push("/");
    },
    exportDocx() {
      jQuery("#docxContent").wordExport("检验报告");
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
  height: 100%;
  padding: 10px 40px;
  width: 100%;
}

table,
th,
td {
  border: 2px solid black;
  border-collapse: collapse;
  text-align: center;
}
</style>
