# Developing-an-expert-adviser-based-on-Parabolic-SAR-indicator
The aim of this study is develop an expert adviser based on parabolic SAR indicator. However, it is necessary to find a trend tracer to combine with this indicator. It was tested diferent moving averages with different periods as trend tracers. Data of different tests are shown and discussed.

**INTRODUCTION**

The parabolic SAR indicator was developed by J. Wells Wilder. This indicator is used by traders to determine trend direction and potential reversals in price. The indicator uses a trailing stop and reverse method called "SAR," or stop and reverse, to identify suitable exit and entry points. Traders also refer to the indicator as to the parabolic stop and reverse or simplely, parabolic SAR. 

**Table 1. Results of the expert adviser using only the parabolic SAR as a buy signal in ITUB4 during 2018-01-01 until 2023-06-09. Only buys made.**
![Table 1 ](https://github.com/Andre-Luis-Lopes-da-Silva/Developing-an-expert-adviser-based-on-Parabolic-SAR-indicator/assets/78765404/eadee7c6-3d40-416b-91ef-e2dcbb3910a8)


**Table 4. Effects of the type and period of moving average in ITUB4 during 2018-01-01 until 2023-06-09. Only buys made. Moving average was used as trend tracer together parabolic SAR.** 
![Table 4](https://github.com/Andre-Luis-Lopes-da-Silva/Developing-an-expert-adviser-based-on-Parabolic-SAR-indicator/assets/78765404/e00e293d-235d-4633-abc4-e5a31657fdfd)


This alteration on code resulted in a small improvement on trades:

bool compra_SAR = velas[1].high > SARValue && mm_Buffer[0]>mm_Buffer[x] && close_atual<Limite;

x corresponding the period of the candle, the distance between the current candle (i.e., mm_Buffer[0]) and previous candle.

See Table 6. 

**Table 6. Results of the expert adviser in BBAS3 (bank sector) during 2018-01-01 until 2023-06-09 using parabolic SAR and smoothed moving average with 21 periods. Only buys made.**
![Table 6](https://github.com/Andre-Luis-Lopes-da-Silva/Developing-an-expert-adviser-based-on-Parabolic-SAR-indicator/assets/78765404/0a3fc123-40dc-4b39-a8b9-176f69301fcb)




