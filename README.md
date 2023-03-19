# Assignment1  
## 策略背景介绍  
宏观动量策略是一种以经济理论为基础的系统化投资策略，区别于趋势跟踪策略只使用资产的价量数据，宏观动量策略采用宏观基本面数据产生交易信号。AQR 在《A Half Century of Macro Momentum》中详细介绍了这种策略，其定义了四种影响标的资产价格的宏观变量，分别为：经济周期、国际贸易、货币政策和风险情绪，其中经济周期又具体分为经济增长和通货膨胀。每个标的资产价格和宏观变量之间都存在着基本的相关关系。例如对于股票而言，经济的增长、通货膨胀的下降、国际贸易竞争力的提高、货币政策的宽松和风险情绪的改善，都是较为明确的看涨信号。海通研报从经济增长、通货膨胀、利率、汇率和风险情绪等多个维度出发构建了宏观动量模型，对股票、债券等大类资产进行月度择时。  
# 因子选取  
从五个角度构建宏观因子，通过宏观因子给出多空信号，构建指数增强策略。  
股票指标选取：  
![image](https://user-images.githubusercontent.com/128219105/226159205-8cbd891d-430f-48b3-b03e-702328a0e680.png)  
债券指标选取：
![image](https://user-images.githubusercontent.com/128219105/226159295-42d0425f-eeba-4c1d-94af-fb62e51ff9cc.png)  
文章结果：
![image](https://user-images.githubusercontent.com/128219105/226159371-c6cf6234-ffdc-4f42-9b14-e05f2a0b9a4d.png)  
# 复现：  
在实际操作中，对于债券的指标有所取舍，未将官方制造业PMI预期误差与CRB指数纳入因子池（数据原因）。  
回测时间：2015/01/31-2023/01/31（因为有些子因子2015年才开始有数据）  
回测过程中在月末将每个小类因子的月度变化方向乘以对资产价格的影响方向得到每个因子的信号（±1、0），再将每个小类因子信号等权相加得到大类因子信号（±1、0），再将每个大类因子信号等权相加得到最终信号，大于 0 买入，等于 0 空仓，小于 0 做空（空仓）。  
# 回测结果：  
股票：  
![image](https://user-images.githubusercontent.com/128219105/226176998-cc89f53b-4b14-49df-a428-1f83aee8949b.png)
![image](https://user-images.githubusercontent.com/128219105/226177017-507345f7-274e-4b3f-91ce-1070bd2a0515.png)  
债券：  
![image](https://user-images.githubusercontent.com/128219105/226177035-fec0daa0-0a47-4d1c-adc4-3b8b5d23f74f.png)
![image](https://user-images.githubusercontent.com/128219105/226177070-d402255f-c81c-4b60-a01c-2b99507f6df2.png)  
综合来讲，宏观因子在股票上的择时效果较好。  

之后对中证500和中证1000也进行了测试，结果如下：  
中证500：  
![image](https://user-images.githubusercontent.com/128219105/226177117-b34eafca-6379-408d-b317-5d80edb31598.png)
![image](https://user-images.githubusercontent.com/128219105/226178282-7c898637-5985-48db-9113-4a0989698845.png)  
中证1000：
![image](https://user-images.githubusercontent.com/128219105/226178292-1b8fe9e6-ddb1-4dc0-b9b8-5d324dfd2fd9.png)
![image](https://user-images.githubusercontent.com/128219105/226178309-d738f311-d2b2-4f35-8e6e-3136c1213614.png)


