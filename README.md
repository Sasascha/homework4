### ETF
VWO,EEM,FXI,EEMV,INDA,AAXJ,MCHI,SPEM,DEM,KWEB,EPI,DGS,ASHR,GXC,AIA,INDY,EIDO,EWM,EDIV,FEM,THD,CQQQ,EWX,EEMA,ESGE,JHEM,GMF,EMQQ,YINN,VNM,KBA,EMGF,EDC,EPHE,SMIN,PIN,PGJ,PIE,SCIF,UEVM,FEMS,CXSE,FNI,ADRE,INCO,DBEM,CHIQ,EUM,CHAU,INDL,YANG,CNYA,EDZ,DGRE,HAO,PEK,CWEB,IDX,NUEM,EEMX,DVEM,FLCH,CN,KURE,FXP,EET,CHIX,CHAD,XPP,INXX,CHIC,MXDE,ASHS,EMDV,OBOR,ASEA,ECNS,YAO,CEZ,EEV,FLAX,CNXT,EMMF,SCIN,WCHN,AXJV,ASHX,AFTY,XCEM,FCA,EMSG,RNEM,YXI,FLIN,LVHE,KGRN,KALL,XINA,KMED,NFTY,CHIL,ISEM,KFYP,REDV,CHIM,PBEE,CHIE,CHII,BCNA,CHIS,CHIK,CHIH,CHIU,CNHX
### 資料來源
Yahoo finance
### 指標類型
1. Sharpe ratio
2. Omega
3. Riskiness

* 計算方式：
均使用三年的時間計算以上指標（156 weeks or 36 months）

### 觀察其中一筆ETF的月資料與週資料分析（EWM）
月資料分布
![月資料分布](https://i.imgur.com/5SH1mIj.png)
月資料PP圖(normal)
![Imgur](https://i.imgur.com/kL9HUrZ.png)
週資料分布
![Imgur](https://i.imgur.com/l8wwTAJ.png)
週資料PP圖(normal)
![Imgur](https://i.imgur.com/yeWwMgk.png)

##### 由上述圖表可知，此ETF的月資料分布較為趨近於常態分佈

### 三個Ratio基於同個x座標的呈現圖
![Imgur](https://i.imgur.com/FEpWvOt.png)

### 衡量三個ratio的rank有多不一樣
* 作法：針對每一檔ETF，衡量三個ratio排名順序的covariance，下方圖中的x座標表示各個ETF，y座標則是covariance的值
![Imgur](https://i.imgur.com/OSNOrkW.png)

##### 可以發現它們的covarance在月資料的表現上不同ETF的變化比較劇烈，但是若以平均來看，月資料或是週資料的covarance都在0.7以上(月：0.7,週：0.78)，排名的結果相當接近。

### 績效評比
* 作法：算出三個ratio之後，根據其挑選表現最好的10之ETF以相同的比例買入（各佔10%），並以rolling window的方式衡量整體的報酬，下圖中x座標為日期，y座標為累計return，其中額外增加三個ratio合再一起的策略('add')
週資料策略 
![Imgur](https://i.imgur.com/lS9TjM9.png)

月資料策略
![Imgur](https://i.imgur.com/SxogfTW.png)

月資料策略詳細版（右上角由上至下改為omega, riskiness, sharp）
![Imgur](https://i.imgur.com/exbQjVm.png)
月資料策略的MDD（由上至下分別為omega, riskiness, sharp）
![Imgur](https://i.imgur.com/cU6uhJD.png)

##### 由上圖可以發現，三種指標做出來的策略整體的報酬走勢大致接近，但若是細部來看，在週資料策略中，表現最好的依序為sharp->riskiness->omega，而在月資料中，表現最好的依序為riskiness->sharp->omega
##### 可以發現sharp對於短週期的表現較好，riskiness對於長週期的表現較好，而omega則是都弱於其他兩者。

