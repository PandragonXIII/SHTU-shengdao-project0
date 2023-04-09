# 生导 proj0



## 思路

> 一些设想： 
>
> 以省为单位设为node，每个node里跑SIR模型，对应4
>
> node之间的距离对应问题中的3
>
> 且随时间改变节点参数：疫苗，季节 对应1，2
>
> 在不同时间解封，对比解封后的疫情形势变化
> html+js



### TODO

**! IMPORTANT: 按省份似乎太多了，要不要大致分为东北华北西北西南东南中部？**

可以在这里留言或者在群里说一下：

> 1. qxy提出
> 2. 

已经在main.html中搭建框架，可以进行进一步填充了

- [x] 显示静态地图和饼状图
- [ ] 写单个省份RIS算法
- [ ] 多个RIS算法以及他们之间的相互作用
- [ ] 动态更新数据
- [ ] ppt
- [ ] （可选）柱状图



#### Echarts 使用指北

1. 配置：本地需要 

   `echarts(.min).js`

   `jquery.js`不清楚是否必须，反正不大

   vscode插件`live server` 

   其他数据文件`*.json`

2. 按格式写

3. vscode中右键 `Open with Live Server` 使用Live Server 打开，不要直接打开html文件



### 题干

2019-nCov病毒带来的传播问题：选择冬季放开防的疫政策是出于什么原则？



查文献，新闻资料来得到数据

数据建模的方式，用模型回答：

1. （扩散模型）考虑低温提高病毒存活时间
2. 考虑疫苗造成的免疫力影响病毒浓度
3. 考虑人员流动造成的传播距离
4. 考虑得病后不再感染



(其实感觉做好可视化是关键？)



## Information

**可以多参考**`chinamap.html` & `map-usa-pie.html` 两个是差不多的，USA可以右键运行，china不能运行

##### 新冠疫情

[感染、死亡、疫苗人数](https://github.com/microsoft/COVID-19-Widget)



[温度对活性影响（简要）](https://kns.cnki.net/KXReader/Detail?invoice=mUPazOX%2FAP4L0hloJBCnFwMYwqLx70MMgJMO%2B3HFU5Rnvv%2B2%2FsPQHb93w0rmm129gfEAy3lyipfCyYAwHK2LTckkfLxLm52u8e2SvIbX3Nle5Ns1FAJuBSBw5hBCTmvGbeqZQoap8bqKIeoCNPFz5Al0UrzEjusXsVAOrunrrwU%3D&DBCODE=CJFD&FileName=ZGDX202103017&TABLEName=cjfdlast2021&nonce=0EAE3F973D914ACE8E2DC2DC9BB142B1&uid=&TIMESTAMP=1675694283869)



类似的结论：不同浓度的新冠病毒在4℃条件下保存较为稳定，均具有感染性；22.5℃条件下，高浓度（10-1稀释度）病毒放置7d感染性逐渐下降，其他较低浓度病毒放置1d则完全失去感染性；37℃保存超过1d病毒即失去感染性。[链接](https://kns.cnki.net/KXReader/Detail?invoice=oqYG2CFDtobP5dj5gNUqmsR2U6gNVT6ocUNH2itnemzSm8JDbofdxiHsYaFB%2BFnz%2BCXSqgjqysR6OY5sqsqFffFC9gnccy5zchWTHyfBFVarDqTPMC0t0%2FuKhl4hs8gwbxIk6%2BiU52WPOxFm5asQOoeZ%2BPsJs9J15L3AO1vYTv0%3D&DBCODE=CJFD&FileName=SHYI202109010&TABLEName=cjfdlast2021&nonce=A2C87E1ACAA543EEBDCC840DFEFA6465&uid=&TIMESTAMP=1675694397094)



[温湿度对新冠传播影响(细致、统计角度)：](https://kns.cnki.net/KXReader/Detail?invoice=KDEm2AmB5OjJIdScN1QWQyvxI5X2V8qPlqA5XFD16MoTOSjorfBRluboTU8wCz048uMTE73oBur0MGy9v1TFKAhpHb1gMllmp%2F0jsPWuog5%2BLhJG62JjyUuXtekrlUhgPtQsZxyZtgNHo11vRj%2B8jFD9TsVV7qpXJ3IapP%2BgUes%3D&DBCODE=CJFD&FileName=HJHX202006003&TABLEName=cjfdlast2020&nonce=E30429CF997A4C1A9B627B1531768130&uid=&TIMESTAMP=1675694759353)



##### 流行病传播模型

[SIR流行病模型简介](https://zhuanlan.zhihu.com/p/496661721)

[现成的算法](https://github.com/tozlucaglar/SIR_model_SEE070) 



##### 可视化

[武汉新型冠状病毒防疫信息收集平台-地图可视化项目](https://github.com/wuhan2020/map-viz) 

[ECharts](https://echarts.apache.org/zh/index.html)可视化工具

[详细教程](https://blog.csdn.net/weixin_43883917/article/details/113886713) 

[教程](https://www.runoob.com/echarts/echarts-tutorial.html) 

[地图+柱状图例子](https://www.makeapie.cn/echarts_content/xxQYhjSh81.html) 

[地图+饼图例子](https://echarts.apache.org/examples/zh/editor.html?c=map-usa-pie) 

[过渡动画](https://echarts.apache.org/handbook/zh/how-to/animation/transition) 



