# ARIMA时序模型

1. 数据预处理；
2. Target做log1p转换，降低其偏度和峰度；
3. 提取训练集中store==1$&item==1的数据做分析；
4. 数据做平稳diff处理；
5. 可视化其自相关、偏自相关、季节性、趋势等特征；
6. 根据结果提取ARIMA的参数(1,1,0)；
    ```
    ARIMA参数order:
      参数1：自回归系数，来自平稳处理后的自相关lag显著个数；
      参数2：平稳阶级，通过多少次diff后平稳；
      参数3：移动平均系数，主要是白噪声相关的，还不知道怎么确认？？？
    ```
7. 可视化预测结果与实际结果，计算rmse值(0.36)；