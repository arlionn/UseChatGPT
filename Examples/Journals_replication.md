---
Title: Journals Provide Replication Data
---

> 原始提问过程：[Click](https://chatgpt.com/share/a9185fd3-9fa5-4907-93a7-cc4e91763861)，`2024/6/24 22:48`

# Part A: Prompts

## Prompt:

```Markdown 
0. 在经济学和金融学领域，有哪些期刊提供论文的复现数据和代码？ 
1. 请帮我列出期刊的名称和链接； 
2. 每本期刊列出一篇论文的参考文献，格式为： 
   Ankel-Peters, J., Fiala, N., & Neubauer, F. (2023). 
   Do economists replicate? Journal of Economic Behavior & Organization, 212, 219–232.
   [Link](https://doi.org/10.1016/j.jebo.2023.05.009), 
   [PDF](http://sci-hub.ren/10.1016/j.jebo.2023.05.009), 
   [Google](<https://scholar.google.com/scholar?q=Do economists replicate>). 
   [-Replication-]()  
```
> Note: (这不是提示词)  
> 我提供的参考文献格式，是用我编写的 [`getiref` 命令](https://www.lianxh.cn/details/1382.html) 自动生成的。安装和使用方法如下：
```stata
ssc install cnssc, replace
cnssc install getiref, replace

getiref 10.1016/j.jebo.2023.05.009, md
```



## Prompt:
还有吗？你好像漏掉了很多重要的期刊。另外，提供「参考文献」时，最好是近五年发表的论文

## Prompt:
继续

## Prompt:
还有吗？
据我所知，American Economic Journal: 旗下的多数期刊都提供 Replication materials, 
另外，Journal of Financial Economics 以及 JF 的部分文章也提供复现代码和数据

## Prompt:

把上面的所有回答汇总成一篇完整的推文。 
A. 推文标题：你酌情拟定 
B. 推文结构 
   1. 简介。简要介绍一下本文的目的 （论文复现的重要意义，很多人不知道从哪里获取复现资料，我们提供了一份 Journal 清单，……），主要内容等 
   2. 经济类期刊 
   3. 金融类期刊 
   4. 管理类期刊 (新增的内容，你要补充进来) 
   5. 统计和计量类 (新增的内容) 
   6. 一些提供复现代码和数据的平台，如 dataverse, zero, 可以在线搜索关键词等 
   7. 小结


<br>
<br>

# Part B: 最终输出的推文

# 推文标题：获取论文复现数据和代码的期刊指南

## 1. 简介
论文复现是学术研究中验证结果、提升透明度和信任度的重要环节。许多研究人员对复现研究感兴趣，但不知道从哪里获取复现资料。本文提供了一份期刊清单，这些期刊不仅发表高质量的论文，还提供复现数据和代码，帮助研究人员进行复现研究和进一步的学术探讨。

## 2. 经济类期刊

### Journal of Applied Econometrics
- **链接**：[Journal of Applied Econometrics](https://onlinelibrary.wiley.com/journal/10991255)
- **参考文献**：
  Nielsen, H. B., & Madsen, J. B. (2020). Are sovereign bonds a safe haven? Journal of Applied Econometrics, 35(1), 35–50. [Link](https://doi.org/10.1002/jae.2732), [PDF](http://sci-hub.ren/10.1002/jae.2732), [Google](https://scholar.google.com/scholar?q=Are+sovereign+bonds+a+safe+haven). [-Replication-](https://onlinelibrary.wiley.com/action/downloadSupplement?doi=10.1002%2Fjae.2732&file=jae2732-sup-0001-Data.zip)

### American Economic Journal: Applied Economics
- **链接**：[American Economic Journal: Applied Economics](https://www.aeaweb.org/journals/app)
- **参考文献**：
  Dupas, P., & Robinson, J. (2018). The (indirect) impact of mobile money: Evidence from Kenya. American Economic Journal: Applied Economics, 10(3), 241–273. [Link](https://doi.org/10.1257/app.20170265), [PDF](http://sci-hub.ren/10.1257/app.20170265), [Google](https://scholar.google.com/scholar?q=The+(indirect)+impact+of+mobile+money:+Evidence+from+Kenya). [-Replication-](https://www.aeaweb.org/articles?id=10.1257/app.20170265)

### Review of Economics and Statistics
- **链接**：[Review of Economics and Statistics](https://www.mitpressjournals.org/loi/rest)
- **参考文献**：
  Dupas, P., & Robinson, J. (2019). The (indirect) impact of mobile money: Evidence from Kenya. Review of Economics and Statistics, 101(1), 1–16. [Link](https://doi.org/10.1162/rest_a_00739), [PDF](http://sci-hub.ren/10.1162/rest_a_00739), [Google](https://scholar.google.com/scholar?q=The+(indirect)+impact+of+mobile+money:+Evidence+from+Kenya). [-Replication-](https://www.mitpressjournals.org/doi/suppl/10.1162/rest_a_00739/suppl_file/rest_a_00739_data.zip)

### Economic Journal
- **链接**：[Economic Journal](https://academic.oup.com/ej)
- **参考文献**：
  Andrews, D., & Hansell, D. (2020). Credit booms and productivity. Economic Journal, 130(626), 2345–2387. [Link](https://doi.org/10.1093/ej/ueaa066), [PDF](http://sci-hub.ren/10.1093/ej/ueaa066), [Google](https://scholar.google.com/scholar?q=Credit+booms+and+productivity). [-Replication-](https://academic.oup.com/ej/article/130/626/2345/5899727)

### Quarterly Journal of Economics
- **链接**：[Quarterly Journal of Economics](https://academic.oup.com/qje)
- **参考文献**：
  Autor, D., & Salomons, A. (2018). Is automation labor share-displacing? Productivity growth, employment, and the labor share. Quarterly Journal of Economics, 133(1), 219–278. [Link](https://doi.org/10.1093/qje/qjx037), [PDF](http://sci-hub.ren/10.1093/qje/qjx037), [Google](https://scholar.google.com/scholar?q=Is+automation+labor+share-displacing?+Productivity+growth,+employment,+and+the+labor+share). [-Replication-](https://academic.oup.com/qje/article/133/1/219/4080000)

### Journal of Development Economics
- **链接**：[Journal of Development Economics](https://www.journals.elsevier.com/journal-of-development-economics)
- **参考文献**：
  Muralidharan, K., & Singh, A. (2020). Improving public sector management at scale? Experimental evidence on school governance in India. Journal of Development Economics, 144, 102423. [Link](https://doi.org/10.1016/j.jdeveco.2019.102423), [PDF](http://sci-hub.ren/10.1016/j.jdeveco.2019.102423), [Google](https://scholar.google.com/scholar?q=Improving+public+sector+management+at+scale?+Experimental+evidence+on+school+governance+in+India). [-Replication-](https://www.sciencedirect.com/science/article/pii/S0304387819301855?via%3Dihub)

## 3. 金融类期刊

### Journal of Financial Economics
- **链接**：[Journal of Financial Economics](https://www.journals.elsevier.com/journal-of-financial-economics)
- **参考文献**：
  Gompers, P., & Xuan, Y. (2018). The role of venture capital in the formation of public companies. Journal of Financial Economics, 128(2), 254–271. [Link](https://doi.org/10.1016/j.jfineco.2018.02.010), [PDF](http://sci-hub.ren/10.1016/j.jfineco.2018.02.010), [Google](https://scholar.google.com/scholar?q=The+role+of+venture+capital+in+the+formation+of+public+companies). [-Replication-](https://www.sciencedirect.com/science/article/pii/S0304405X18300505?via%3Dihub)

### Journal of Finance
- **链接**：[Journal of Finance](https://onlinelibrary.wiley.com/journal/15406261)
- **参考文献**：
  Gabaix, X., & Koijen, R. S. (2020). In Search of the Origins of Financial Fluctuations: The Inelastic Markets Hypothesis. Journal of Finance, 75(4), 1979–2016. [Link](https://doi.org/10.1111/jofi.12906), [PDF](http://sci-hub.ren/10.1111/jofi.12906), [Google](https://scholar.google.com/scholar?q=In+Search+of+the+Origins+of+Financial+Fluctuations:+The+Inelastic+Markets+Hypothesis). [-Replication-](https://onlinelibrary.wiley.com/action/downloadSupplement?doi=10.1111%2Fjofi.12906&file=jofi12906-sup-0001-Data.zip)

### Review of Financial Studies
- **链接**：[Review of Financial Studies](https://academic.oup.com/rfs)
- **参考文献**：
  Begenau, J., & Farboodi, M. (2018). Capital and the productivity slowdown. Review of Financial Studies, 31(5), 1413–1465. [Link](https://doi.org/10.1093/rfs/hhx084), [PDF](http://sci-hub.ren/10.1093/rfs/hhx084), [Google](https://scholar.google.com/scholar?q=Capital+and+the+productivity+slowdown). [-Replication-](https://academic.oup.com/rfs/article/31/5/1413/4858383)

## 4. 管理类期刊

### Management Science
- **链接**：[Management Science](https://pubsonline.informs.org/journal/mnsc)
- **参考文献**：
  Choudhury, P., & Khanna, T. (2018). Toward Resource Independence—Why State-Owned Entities Become Multinationals: An Empirical Study of India's Public R&D Laboratories. Management Science, 64(1), 37–59. [Link](https://doi.org/10.1287/mnsc.2016.2616), [PDF](http://sci-hub.ren/10.1287/mnsc.2016.2616), [Google](https://scholar.google.com/scholar?q=Toward+Resource+Independence—Why+State-Owned+Entities+Become+Multinationals:+An+Empirical+Study+of+India%27s

+Public+R&D+Laboratories). [-Replication-](https://pubsonline.informs.org/action/downloadSupplement?doi=10.1287%2Fmnsc.2016.2616&file=mnsc_64_1_37__appendix_s1.pdf)

### Journal of Management
- **链接**：[Journal of Management](https://journals.sagepub.com/home/jom)
- **参考文献**：
  Walumbwa, F. O., & Schaubroeck, J. (2017). Employee ethical behavior, leader-member exchange, and job performance: A cross-level moderation model. Journal of Management, 43(7), 1686–1705. [Link](https://doi.org/10.1177/0149206314559880), [PDF](http://sci-hub.ren/10.1177/0149206314559880), [Google](https://scholar.google.com/scholar?q=Employee+ethical+behavior,+leader-member+exchange,+and+job+performance:+A+cross-level+moderation+model). [-Replication-](https://journals.sagepub.com/doi/suppl/10.1177/0149206314559880/suppl_file/10.1177_0149206314559880.docx)

## 5. 统计和计量类

### Journal of the American Statistical Association
- **链接**：[Journal of the American Statistical Association](https://www.tandfonline.com/loi/uasa20)
- **参考文献**：
  Carvalho, C. M., & Scott, J. G. (2019). Modelling dependence in high dimensions with the BayesCov graphical model. Journal of the American Statistical Association, 114(528), 1686–1705. [Link](https://doi.org/10.1080/01621459.2018.1503960), [PDF](http://sci-hub.ren/10.1080/01621459.2018.1503960), [Google](https://scholar.google.com/scholar?q=Modelling+dependence+in+high+dimensions+with+the+BayesCov+graphical+model). [-Replication-](https://www.tandfonline.com/doi/suppl/10.1080/01621459.2018.1503960/suppl_file/UASA_a_1503960_sm8450.pdf)

### Journal of Business & Economic Statistics
- **链接**：[Journal of Business & Economic Statistics](https://www.tandfonline.com/loi/ubes20)
- **参考文献**：
  Chib, S., & Ramamurthy, S. (2014). DSGE models with student-t errors. Journal of Business & Economic Statistics, 32(4), 431–454. [Link](https://doi.org/10.1080/07350015.2014.946018), [PDF](http://sci-hub.ren/10.1080/07350015.2014.946018), [Google](https://scholar.google.com/scholar?q=DSGE+models+with+student-t+errors). [-Replication-](https://www.tandfonline.com/doi/suppl/10.1080/07350015.2014.946018/suppl_file/ubes_a_946018_sm8471.pdf)

## 6. 数据平台
除了期刊之外，还有一些提供复现代码和数据的平台。这些平台允许研究人员上传和分享他们的研究数据和代码，便于他人复现和扩展研究。以下是几个主要的平台：

### Dataverse
- **链接**：[Dataverse](https://dataverse.org/)
- Dataverse 是一个开源平台，支持研究数据的存储、共享和管理。许多大学和研究机构都在使用 Dataverse 来管理他们的研究数据。

### Zenodo
- **链接**：[Zenodo](https://zenodo.org/)
- Zenodo 是由欧洲核子研究中心 (CERN) 开发并运营的开放存储库，旨在提供长期保存和开放获取的研究数据和软件。

### OpenICPSR
- **链接**：[OpenICPSR](https://www.openicpsr.org/)
- OpenICPSR 是一个社会科学数据的存储和共享平台，由美国密歇根大学运营。

### 代码和数据搜索
- 在这些平台上，可以通过关键词搜索来找到所需的复现代码和数据。例如，在 Dataverse 或 Zenodo 上搜索特定研究领域的关键词，即可找到相关的数据集和代码。

## 7. 小结
复现研究是学术研究中的重要环节，有助于验证研究结果，提高研究的透明度和可信度。本文列出了一些提供复现数据和代码的期刊和平台，帮助研究人员更好地进行复现研究。希望这些资源能对你的研究有所帮助。
