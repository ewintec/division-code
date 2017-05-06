# 中国行政区划代码数据

## 编码规则 引自[维基百科](https://zh.wikipedia.org/wiki/%E4%B8%AD%E5%8D%8E%E4%BA%BA%E6%B0%91%E5%85%B1%E5%92%8C%E5%9B%BD%E8%A1%8C%E6%94%BF%E5%8C%BA%E5%88%92%E4%BB%A3%E7%A0%81)

> 代码从左至右的含义是：  
&emsp;&emsp;第一、二位表示省级行政单位（省、自治区、直辖市、特别行政区），其中第一位代表大区。  
&emsp;&emsp;第三、四位表示地级行政单位（地级市、地区、自治州、盟及省级单位直属县级单位的汇总码）。  
&emsp;&emsp;&emsp;&emsp;对于省（自治区）下属单位：01-20，51-70表示省辖市（地级市）；21-50表示地区（自治州、盟）；90表示省（自治区）直辖县级行政区划的汇总。  
&emsp;&emsp;&emsp;&emsp;对于直辖市下属单位：01表示市辖区的汇总；02表示县的汇总。  
&emsp;&emsp;第五、六位表示县级行政单位（县、自治县、市辖区、县级市、旗、自治旗、林区、特区）。  
&emsp;&emsp;&emsp;&emsp;对于地级市下属单位：01-20表示市辖区（特区）；21-80表示县（旗、自治县、自治旗、林区）；81-99表示地级市代管的县级市。  
&emsp;&emsp;&emsp;&emsp;对于直辖市所辖县级行政单位：01-20、51-80代表市辖区；21-50代表县（自治县）。  
&emsp;&emsp;&emsp;&emsp;对于地区（自治州、盟）下属单位：01-20表示县级市；21-80表示县（旗、自治县、自治旗）。  
&emsp;&emsp;&emsp;&emsp;对于省级直辖县级行政单位：同地区。


## 数据来源：

* [中华人民共和国国家统计局-2015年统计用区划代码和城乡划分代码(截止2015年09月30日)](http://www.stats.gov.cn/tjsj/tjbz/tjyqhdmhcxhfdm/2015/index.html)

* [中华人民共和国民政部-中华人民共和国行政区划代码](http://www.mca.gov.cn/article/sj/tjbz/a/)

* [中华人民共和国民政部-2017年2月中华人民共和国县以上行政区划代码](http://www.mca.gov.cn/article/sj/tjbz/a/2017/0327/2017%E5%B9%B42%E6%9C%88%E4%B8%AD%E5%8D%8E%E4%BA%BA%E6%B0%91%E5%85%B1%E5%92%8C%E5%9B%BD%E5%8E%BF%E4%BB%A5%E4%B8%8A%E8%A1%8C%E6%94%BF%E5%8C%BA%E5%88%92%E4%BB%A3%E7%A0%81.html)

* [中华人民共和国民政部-2013年中华人民共和国县以下行政区划代码](http://files2.mca.gov.cn/cws/201404/20140404125738290.htm)

* [中华人民共和国国家统计局-最新县及县以上行政区划代码（截止2016年7月31日）](http://www.stats.gov.cn/tjsj/tjbz/xzqhdm/201703/t20170310_1471429.html)

* [博雅地名分享网](http://www.tcmap.com.cn/)

## 用法

```js
npm install
npm run start:official         // 获取官方数据
npm run start:unofficial       // 博雅地名网数据
```

## VSCode 调试配置文件 launch.json

```json
{
  "version": "0.2.0",
  "configurations": [{
    "type": "node",
    "request": "launch",
    "name": "启动程序",
    "program": "${workspaceRoot\\division-code\\official\\index.js"
  }]
}
```

## 提示：

    县级以上区划代码：以民政部 2017/02 区划代码为准
    县级以下区划代码：13年和15年两份数据有差异，15年以后县级以下只提供变更，可以爬数据 update 数据
    博雅地名分享网：  提供数据，对比民政部的变更，数据比较新，不过是分散在各个页面

