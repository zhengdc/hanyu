<template>
  <div>
    <div class="joinbanenr">
        <h2>欢迎加入我们</h2>
        <p>加入翰禹，成就梦想！</p>
    </div>
    <div class="joinContent">
        <div class="cont">
          <el-row :gutter="30">
            <el-col :span="8" style="line-height: 35px;">
              <h3>公司介绍</h3>
              <p>工作时间：周一～周五 9：00-18：00</p>
              <p>工作地点：杭州市萧山区祥腾财富中心 2幢2002室。</p>
              <p>咨询电话：0571-82666642</p>
            </el-col>
            <el-col :span="16" style="border-left:2px solid #FFA500;;">
              <p class="job"><span>职位名称</span></p>
              <el-collapse v-model="activeName" accordion>
                <el-collapse-item title="产品经理" name="1">
                  <h3>岗位描述：</h3>
                  <p>1、负责产品用户研究, 竞争产品分析, 产品规划构思和创意过程</p>
                  <p>2、根据需求和用户研究的结果, 完成界面的信息架构, 流程和原型设计、编写技术需求文档</p>
                  <p>3、运用相关工具，快速完成idea到prototype的转化</p>
                  <h3>任职要求：</h3>
                  <p>1、本科及以上学历，3年以上产品管理工作经验</p>
                  <p>2、热爱互联网行业，重视产品用户体验，富有创新精神，对互联网和移动互联网的发展具有 敏锐的嗅觉 </p>
                  <p>3、具备互联网、移动互联网产品的管理能力与策划能力，熟知互联网或软件产品整体实现过程</p>
                </el-collapse-item>
                <el-collapse-item title="渠道推广经理" name="2">
                  <h3>岗位描述：</h3>
                  <p>1、负责产品用户研究, 竞争产品分析, 产品规划构思和创意过程</p>
                  <p>2、根据需求和用户研究的结果, 完成界面的信息架构, 流程和原型设计、编写技术需求文档</p>
                  <p>3、运用相关工具，快速完成idea到prototype的转化</p>
                  <h3>任职要求：</h3>
                  <p>1、本科及以上学历，3年以上产品管理工作经验</p>
                  <p>2、热爱互联网行业，重视产品用户体验，富有创新精神，对互联网和移动互联网的发展具有 敏锐的嗅觉 </p>
                  <p>3、具备互联网、移动互联网产品的管理能力与策划能力，熟知互联网或软件产品整体实现过程</p>
                </el-collapse-item>
                <el-collapse-item title="审核专员" name="3">
                  <h3>岗位描述：</h3>
                  <p>1、负责产品用户研究, 竞争产品分析, 产品规划构思和创意过程</p>
                  <p>2、根据需求和用户研究的结果, 完成界面的信息架构, 流程和原型设计、编写技术需求文档</p>
                  <p>3、运用相关工具，快速完成idea到prototype的转化</p>
                  <h3>任职要求：</h3>
                  <p>1、本科及以上学历，3年以上产品管理工作经验</p>
                  <p>2、热爱互联网行业，重视产品用户体验，富有创新精神，对互联网和移动互联网的发展具有 敏锐的嗅觉 </p>
                  <p>3、具备互联网、移动互联网产品的管理能力与策划能力，熟知互联网或软件产品整体实现过程</p>
                </el-collapse-item>
              </el-collapse>
            </el-col>
          </el-row>
        </div>
    </div>
  </div>

</template>

<script>
  export default{
    data(){
      return{
        activeName:1
      }
    }
  }
</script>
