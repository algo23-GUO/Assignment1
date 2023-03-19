# Assignment1
从五个角度构建宏观因子，通过宏观因子给出多空信号，构建指数增强策略。  
股票指标选取：  
![image](https://user-images.githubusercontent.com/128219105/226159205-8cbd891d-430f-48b3-b03e-702328a0e680.png)  
债券指标选取：
![image](https://user-images.githubusercontent.com/128219105/226159295-42d0425f-eeba-4c1d-94af-fb62e51ff9cc.png)  
文章结果：
![image](https://user-images.githubusercontent.com/128219105/226159371-c6cf6234-ffdc-4f42-9b14-e05f2a0b9a4d.png)  
复现：  
在实际操作中，对于债券的指标有所取舍，未将官方制造业PMI预期误差与CRB指数纳入因子池（数据原因）。  
回测时间：2015/01/31-2023/01/31（因为有些子因子2015年才开始有数据）  
回测结果：  
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


