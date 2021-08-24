# litemall

又一个小商场系统。

litemall = Spring Boot后端 + Vue管理员前端 + 微信小程序用户前端 + Vue用户移动端

* [文档](https://linlinjava.gitbook.io/litemall)
* [贡献](https://linlinjava.gitbook.io/litemall/contribute)
* [FAQ](https://linlinjava.gitbook.io/litemall/faq)
* [API](https://linlinjava.gitbook.io/litemall/api)

## 项目实例

### 小商场实例

* renard-wx模块实例

![](./doc/pics/readme/renard_wx_demo.png)

> 注意：此实例是真实小商场，开发者可以购买商品和付款，但请不要尝试退款操作。

* litemall-wx模块实例

![](./doc/pics/readme/litemall_wx_demo.png)

> 注意：此实例是测试小商场，开发者请不要尝试购买商品、付款、退款操作。

### 轻商场实例

请手机扫描以下二维码访问:

![](./doc/pics/readme/mobmall.png)

或者浏览器采用手机模式访问以下网址: [http://122.51.199.160:8080/vue/index.html#/](http://122.51.199.160:8080/vue/index.html#/)

注意：
> 1. 由于第一次加载数据量较大，建议wifi网络访问，且耐心等待数秒。
> 2. 此实例是测试轻商场，不支持支付，而且处于开发中还不完善。

### 管理后台实例

![](./doc/pics/readme/admin-dashboard.png)

1. 浏览器打开，输入以下网址: [http://122.51.199.160:8080/#/login](http://122.51.199.160:8080/#/login)
2. 管理员用户名`admin123`，管理员密码`admin123`
> 注意：此实例只是测试管理后台，不是前两个小商城的管理后台。

## 项目代码

* [码云](https://gitee.com/linlinjava/litemall)
* [GitHub](https://github.com/linlinjava/litemall)

## 项目架构
![](./doc/pics/readme/project-structure.png)

## 技术栈

> 1. Spring Boot
> 2. Vue
> 3. 微信小程序

![](doc/pics/readme/technology-stack.png)

## 功能

### 小商城功能

* 首页
* 专题列表、专题详情
* 分类列表、分类详情
* 品牌列表、品牌详情
* 新品首发、人气推荐
* 优惠券列表、优惠券选择
* 团购
* 搜索
* 商品详情、商品评价、商品分享
* 购物车
* 下单
* 订单列表、订单详情、订单售后
* 地址、收藏、足迹、意见反馈
* 客服

### 管理平台功能

* 会员管理
* 商城管理
* 商品管理
* 推广管理
* 系统管理
* 配置管理
* 统计报表

## 快速启动

1. 配置最小开发环境：
    * [MySQL](https://dev.mysql.com/downloads/mysql/)
    * [JDK1.8或以上](http://www.oracle.com/technetwork/java/javase/overview/index.html)
    * [Maven](https://maven.apache.org/download.cgi)
    * [Nodejs](https://nodejs.org/en/download/)
    * [微信开发者工具](https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html)
    
2. 数据库依次导入litemall-db/sql下的数据库文件
    * litemall_schema.sql
    * litemall_table.sql
    * litemall_data.sql

3. 启动小商场和管理后台的后端服务

    打开命令行，输入以下命令
    ```bash
    cd litemall
    mvn install
    mvn clean package
    java -Dfile.encoding=UTF-8 -jar litemall-all/target/litemall-all-0.1.0-exec.jar
    ```
    
4. 启动管理后台前端

    打开命令行，输入以下命令
    ```bash
    npm install -g cnpm --registry=https://registry.npm.taobao.org
    cd litemall/litemall-admin
    cnpm install
    cnpm run dev
    ```
    此时，浏览器打开，输入网址`http://localhost:9527`, 此时进入管理后台登录页面。
    
5. 启动小商城前端
   
   这里存在两套小商场前端litemall-wx和renard-wx，开发者可以分别导入和测试：
   
   1. 微信开发工具导入litemall-wx项目;
   2. 项目配置，启用“不校验合法域名、web-view（业务域名）、TLS 版本以及 HTTPS 证书”
   3. 点击“编译”，即可在微信开发工具预览效果；
   4. 也可以点击“预览”，然后手机扫描登录（但是手机需开启调试功能）。
      
   注意：
   > 这里只是最简启动方式，而小商场的微信登录、微信支付等功能需开发者设置才能运行，
   > 更详细方案请参考[文档](https://linlinjava.gitbook.io/litemall/project)。

6. 启动轻商城前端

    打开命令行，输入以下命令
    ```bash
    npm install -g cnpm --registry=https://registry.npm.taobao.org
    cd litemall/litemall-vue
    cnpm install
    cnpm run dev
    ```
    此时，浏览器（建议采用chrome 手机模式）打开，输入网址`http://localhost:6255`, 此时进入轻商场。

    注意：
    > 现在功能很不稳定，处在开发阶段。
        
## 开发计划

当前版本[v1.7.0](https://linlinjava.gitbook.io/litemall/changelog)

目前项目开发中，存在诸多不足，以下是目前规划的开发计划。

V 1.0.0 完成以下目标：

1. 除了部分功能（如优惠券等），小商城的优化和改进基本结束；
2. 管理后台基本实现所有表的CRUD操作；
3. 后端服务能够对参数进行检验。

V 2.0.0 完成以下目标：

1. 小商城和管理后台完成所有基本业务；
2. 管理后台实现统计功能、日志功能、权限功能；
3. 业务代码和细节代码进行调整优化；
4. 轻商城的开发；

V 3.0.0 完成以下目标：

1. 管理后台一些辅助功能
2. 后端服务加强安全功能、配置功能
3. 缓存功能以及优化一些性能

## 警告

> 1. 本项目仅用于学习练习
> 2. 本项目还不完善，仍处在开发中，不承担任何使用后果
> 3. 本项目代码开源[MIT](./LICENSE)，项目文档采用 [署名-禁止演绎 4.0 国际协议许可](https://creativecommons.org/licenses/by-nd/4.0/deed.zh)

## 致谢

本项目基于或参考以下项目：

1. [nideshop-mini-program](https://github.com/tumobi/nideshop-mini-program)

   项目介绍：基于Node.js+MySQL开发的开源微信小程序商城（微信小程序）

   项目参考：
   
   1. litemall项目数据库基于nideshop-mini-program项目数据库；
   2. litemall项目的litemall-wx模块基于nideshop-mini-program开发。

2. [vue-element-admin](https://github.com/PanJiaChen/vue-element-admin)
  
   项目介绍： 一个基于Vue和Element的后台集成方案
  
   项目参考：litemall项目的litemall-admin模块的前端框架基于vue-element-admin项目修改扩展。

3. [mall-admin-web](https://github.com/macrozheng/mall-admin-web)

   项目介绍：mall-admin-web是一个电商后台管理系统的前端项目，基于Vue+Element实现。

   项目参考：litemall项目的litemall-admin模块的一些页面布局样式参考了mall-admin-web项目。

4. [biu](https://github.com/CaiBaoHong/biu)

   项目介绍：管理后台项目开发脚手架，基于vue-element-admin和springboot搭建，前后端分离方式开发和部署。

   项目参考：litemall项目的权限管理功能参考了biu项目。

5. [vant--mobile-mall](https://github.com/qianzhaoy/vant--mobile-mall)

   项目介绍：基于有赞 vant 组件库的移动商城。

   项目参考：litemall项目的litemall-vue模块基于vant--mobile-mall项目开发。

## 推荐

1. [Flutter_Mall](https://github.com/youxinLu/mall)
   
   项目介绍：Flutter_Mall是一款Flutter开源在线商城应用程序。
   
2. [Taro_Mall](https://github.com/jiechud/taro-mall)

    项目介绍：Taro_Mall是一款多端开源在线商城应用程序，后台是基于litemall基础上进行开发，前端采用Taro框架编写。


## 问题

![](doc/pics/readme/qq3.png)

 * 开发者有问题或者好的建议可以用Issues反馈交流，请给出详细信息
 * 在开发交流群中应讨论开发、业务和合作问题
 * 如果真的需要QQ群里提问，请在提问前先完成以下过程：
    * 请仔细阅读本项目文档，特别是是[**FAQ**](https://linlinjava.gitbook.io/litemall/faq)，查看能否解决；
    * 请阅读[提问的智慧](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way/blob/master/README-zh_CN.md)；
    * 请百度或谷歌相关技术；
    * 请查看相关技术的官方文档，例如微信小程序的官方文档；
    * 请提问前尽可能做一些DEBUG或者思考分析，然后提问时给出详细的错误相关信息以及个人对问题的理解。

## License

[MIT](https://github.com/linlinjava/litemall/blob/master/LICENSE)
Copyright (c) 2018-present linlinjava


```vue
   <template>
  <div class="app-container">

    <div class="table-layout">
      <el-row>
        <el-col :span="4" class="table-cell-title">名称</el-col>
        <el-col :span="4" class="table-cell-title">介绍名称</el-col>
        <el-col :span="4" class="table-cell-title">标签</el-col>
        <el-col :span="4" class="table-cell-title">优惠券类型</el-col>
        <el-col :span="4" class="table-cell-title">最低消费</el-col>
        <el-col :span="4" class="table-cell-title">优惠面值</el-col>
      </el-row>
      <el-row>
        <el-col :span="4" class="table-cell">{{ coupon.name }}</el-col>
        <el-col :span="4" class="table-cell">{{ coupon.desc }}</el-col>
        <el-col :span="4" class="table-cell">{{ coupon.tag }}</el-col>
        <el-col :span="4" class="table-cell">{{ coupon.type | formatType }}</el-col>
        <el-col :span="4" class="table-cell">满{{ coupon.min }}元可用</el-col>
        <el-col :span="4" class="table-cell">减免{{ coupon.discount }}元</el-col>
      </el-row>
      <el-row>
        <el-col :span="4" class="table-cell-title">每人限额</el-col>
        <el-col :span="4" class="table-cell-title">当前状态</el-col>
        <el-col :span="4" class="table-cell-title">商品范围</el-col>
        <el-col :span="4" class="table-cell-title">有效期</el-col>
        <el-col :span="4" class="table-cell-title">优惠兑换码</el-col>
        <el-col :span="4" class="table-cell-title">发行数量</el-col>
      </el-row>
      <el-row>
        <el-col :span="4" class="table-cell">{{ coupon.limit }}</el-col>
        <el-col :span="4" class="table-cell">{{ coupon.status | formatStatus }}</el-col>
        <el-col :span="4" class="table-cell">{{ coupon.goodsType | formatGoodsType }}</el-col>
        <el-col :span="4" class="table-cell">{{ getTimeScope() }}</el-col>
        <el-col :span="4" class="table-cell">{{ coupon.code }}</el-col>
        <el-col :span="4" class="table-cell">{{ coupon.total === 0 ? "不限" : coupon.total }}</el-col>
      </el-row>
    </div>

    <!-- 查询操作 -->
    <div class="filter-container">

      <!-- 根据用户id查询 -->
      <el-input v-model="listQuery.userId" clearable 
      class="filter-item" style="width: 200px;" placeholder="请输入用户ID"/>
      
      <!-- 查询状态 -->
      <el-select v-model="listQuery.status" clearable 
      style="width: 200px" class="filter-item" placeholder="请选择使用状态">
      
        <el-option v-for="type in useStatusOptions" 
        :key="type.value" 
        :label="type.label" 
        :value="type.value"/>
      </el-select>

      <!-- 查询按钮 -->
      <el-button v-permission="['GET /admin/coupon/listuser']" class="filter-item" type="primary" icon="el-icon-search" @click="handleFilter">查找</el-button>
    </div>

    <!-- 查询结果 -->
    <el-table v-loading="listLoading" :data="list" element-loading-text="正在查询中。。。" border fit highlight-current-row>
      <el-table-column align="center" label="用户优惠券ID" prop="id" sortable/>
      <el-table-column align="center" label="用户ID" prop="userId"/>
      <el-table-column align="center" label="领取时间" prop="addTime"/>
      <el-table-column align="center" label="使用状态" prop="status">
        <template slot-scope="scope">{{ scope.row.status | formatUseStatus }}</template>
      </el-table-column>
      <el-table-column align="center" label="订单ID" prop="orderId"/>
      <el-table-column align="center" label="使用时间" prop="usedTime"/>
    </el-table>

    <pagination v-show="total>0" :total="total" :page.sync="listQuery.page" :limit.sync="listQuery.limit" @pagination="getList" />

  </div>
</template>

<script>
import { readCoupon, listCouponUser } from '@/api/coupon'
import Pagination from '@/components/Pagination' // Secondary package based on el-pagination

const defaultTypeOptions = [
  {
    label: '通用领券',
    value: 0
  },
  {
    label: '注册赠券',
    value: 1
  },
  {
    label: '兑换码',
    value: 2
  }
]

const defaultUseStatusOptions = [
  {
    label: '未使用',
    value: 0
  },
  {
    label: '已使用',
    value: 1
  },
  {
    label: '已过期',
    value: 2
  },
  {
    label: '已下架',
    value: 3
  }
]

export default {
  name: 'CouponDetail',
  components: { Pagination },
  filters: {
    formatType(type) {
      for (let i = 0; i < defaultTypeOptions.length; i++) {
        if (type === defaultTypeOptions[i].value) {
          return defaultTypeOptions[i].label
        }
      }
      return ''
    },
    formatGoodsType(goodsType) {
      if (goodsType === 0) {
        return '全场通用'
      } else if (goodsType === 1) {
        return '指定分类'
      } else {
        return '指定商品'
      }
    },
    formatStatus(status) {
      if (status === 0) {
        return '正常'
      } else if (status === 1) {
        return '已过期'
      } else {
        return '已下架'
      }
    },
    formatUseStatus(status) {
      if (status === 0) {
        return '未使用'
      } else if (status === 1) {
        return '已使用'
      } else if (status === 3) {
        return '已过期'
      } else {
        return '已下架'
      }
    }
  },
  data() {
    return {
      typeOptions: Object.assign({}, defaultTypeOptions),
      useStatusOptions: Object.assign({}, defaultUseStatusOptions),
      coupon: {},
      list: [],  //这里接收优惠券的使用情况
      total: 0,
      listLoading: true,

      listQuery: {    //列表查询的参数
        page: 1,
        limit: 20,
        couponId: 0,      //初始优惠券id
        userId: undefined,  //初始用户id *****主要*******
        status: undefined,
        sort: 'add_time',
        order: 'desc'
      },
      downloadLoading: false
    }
  },
  created() {
    this.init()
  },
  methods: {
    init: function() {
      if (this.$route.query.id == null) {
        return
      }
      readCoupon(this.$route.query.id).then(response => {
        this.coupon = response.data.data  //优惠券详情获取
      })
      this.listQuery.couponId = this.$route.query.id   //获取所有的这个优惠券使用情况 的优惠id
      this.getList()
    },
    getList() {     //下面列表的获取方法
      this.listLoading = true
      listCouponUser(this.listQuery)   //将参数传进这个 用户使用优惠券的方法中
        .then(response => {
          this.list = response.data.data.list
          this.total = response.data.data.total
          this.listLoading = false
        })
        .catch(() => {
          this.list = []
          this.total = 0
          this.listLoading = false
        })
    },
    handleFilter() {
      this.listQuery.page = 1
      this.getList()
    },
    getTimeScope() {
      if (this.coupon.timeType === 0) {
        return '领取' + this.coupon.days + '天有效'
      } else if (this.coupon.timeType === 1) {
        return '自' + this.coupon.startTime + '至' + this.coupon.endTime + '有效'
      } else {
        return '未知'
      }
    },
    getGoodsScope() {
    }
  }
}
</script>
<style scoped>
  .filter-container {
    margin-top: 20px;
  }

  .table-layout {
    margin-top: 20px;
    border-left: 1px solid #DCDFE6;
    border-top: 1px solid #DCDFE6;
  }
  .table-cell {
    height: 60px;
    line-height: 40px;
    border-right: 1px solid #DCDFE6;
    border-bottom: 1px solid #DCDFE6;
    padding: 10px;
    font-size: 14px;
    color: #606266;
    text-align: center;
    overflow: hidden;
  }
  .table-cell-title {
    border-right: 1px solid #DCDFE6;
    border-bottom: 1px solid #DCDFE6;
    padding: 10px;
    background: #F2F6FC;
    text-align: center;
    font-size: 14px;
    color: #303133;
  }
</style>

```



```java
   @GetMapping("/listuser")
    public Object listuser(Integer userId, Integer couponId, Short status,
                           @RequestParam(defaultValue = "1") Integer page,
                           @RequestParam(defaultValue = "10") Integer limit,
                           @Sort @RequestParam(defaultValue = "add_time") String sort,
                           @Order @RequestParam(defaultValue = "desc") String order) {
        List<LitemallCouponUser> couponList = couponUserService.queryList(userId, couponId, status, page,
                limit, sort, order);
        return ResponseUtil.okList(couponList);
    }
```
