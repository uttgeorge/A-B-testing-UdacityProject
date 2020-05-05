# Project Overview

## Experiment Overview: Free Trial Screener

At the time of this experiment, Udacity courses currently have two options on the course overview page: "start free trial", and "access course materials". If the student clicks "start free trial", they will be asked to enter their credit card information, and then they will be enrolled in a free trial for the paid version of the course. After 14 days, they will automatically be charged unless they cancel first. If the student clicks "access course materials", they will be able to view the videos and take the quizzes for free, but they will not receive coaching support or a verified certificate, and they will not submit their final project for feedback.

In the experiment, Udacity tested a change where if the student clicked "start free trial", they were asked how much time they had available to devote to the course. If the student indicated 5 or more hours per week, they would be taken through the checkout process as usual. If they indicated fewer than 5 hours per week, a message would appear indicating that Udacity courses usually require a greater time commitment for successful completion, and suggesting that the student might like to access the course materials for free. At this point, the student would have the option to continue enrolling in the free trial, or access the course materials for free instead. This screenshot shows what the experiment looks like.

![](https://github.com/uttgeorge/abtesting_Free-Trial-Screener/blob/master/files/Final%20Project_%20Experiment%20Screenshot.png)

The hypothesis was that this might set clearer expectations for students upfront, thus reducing the number of frustrated students who left the free trial because they didn't have enough time—without significantly reducing the number of students to continue past the free trial and eventually complete the course. If this hypothesis held true, Udacity could improve the overall student experience and improve coaches' capacity to support students who are likely to complete the course.

The unit of diversion is a cookie, although if the student enrolls in the free trial, they are tracked by user-id from that point forward. The same user-id cannot enroll in the free trial twice. For users that do not enroll, their user-id is not tracked in the experiment, even if they were signed in when they visited the course overview page.

## Metric Choice

Which of the following metrics would you choose to measure for this experiment and why? For each metric you choose, indicate whether you would use it as an invariant metric or an evaluation metric. The practical significance boundary for each metric, that is, the difference that would have to be observed before that was a meaningful change for the business, is given in parentheses. All practical significance boundaries are given as absolute changes.

Any place "unique cookies" are mentioned, the uniqueness is determined by day. (That is, the same cookie visiting on different days would be counted twice.) User-ids are automatically unique since the site does not allow the same user-id to enroll twice.

- Number of cookies: That is, number of unique cookies to view the course overview page. (dmin=3000)

- Number of user-ids: That is, number of users who enroll in the free trial. (dmin=50)

Number of clicks: That is, number of unique cookies to click the "Start free trial" button (which happens before the free trial screener is trigger). (dmin=240)

Click-through-probability: That is, number of unique cookies to click the "Start free trial" button divided by number of unique cookies to view the course overview page. (dmin=0.01)

Gross conversion: That is, number of user-ids to complete checkout and enroll in the free trial divided by number of unique cookies to click the "Start free trial" button. (dmin= 0.01)

Retention: That is, number of user-ids to remain enrolled past the 14-day boundary (and thus make at least one payment) divided by number of user-ids to complete checkout. (dmin=0.01)

Net conversion: That is, number of user-ids to remain enrolled past the 14-day boundary (and thus make at least one payment) divided by the number of unique cookies to click the "Start free trial" button. (dmin= 0.0075)

You should also decide now what results you will be looking for in order to launch the experiment. Would a change in any one of your evaluation metrics be sufficient? Would you want to see multiple metrics all move or not move at the same time in order to launch? This decision will inform your choices while designing the experiment.


# 编程往事
大一的时候，谈到“技术”宅，同学们更多想到的是会PS，会装系统。跟风学了一些PS、Dreamweaver，但也不得要领。“世界末日”后两个月， 一个普通的寒假，发生了一些微妙地事，然后经过化学反应最终变成蝴蝶效应（可参考：[果冻虾仁：大家是如何走向计算机编程的这条路的？又如何坚持不懈的深入学习？到底最初的动机是什么？](https://www.zhihu.com/question/60865334/answer/182169005)）。

然后在除夕夜，QQ空间里发了一条说说，算是立了一个Flag“新的一年开始混CSDN了”。

![](https://pic4.zhimg.com/80/v2-ccb132273a6e6f8aa70545939c51bc38_hd.jpg)


我确实有过很多失败的Flag，但这一次绝对是完成度比较高的一个。后面不仅混了一年CSDN，甚至混了整个大学的CSDN，从看博文到写博客。主要是一次闲来无事写了一篇文章，然后上了CSDN的首页推荐，从此我对写作的热情一发不可收拾。从流水账式的代码记录到开始慢慢地用心去写，可是后来再也没有上过首页了……哈哈。如今看来当时的很多技术博文十分稚嫩，但对于当时更为稚嫩的自己却是一种更大的鼓励了。大学的经历这里不再一一介绍了，CSDN博客中有一个系列文章：[编程往事](https://blog.csdn.net/guodongxiaren/article/category/1374165) 。有兴趣可以阅读。

# 文章比代码写的好？
上大学的时候也有段时间持续地输出技术文章，但是一直不瘟不火。可能是技术太菜了，后面写的一些个人经历，感悟之类的，比如上面提到的“[编程往事](https://blog.csdn.net/guodongxiaren/article/category/1374165)”系列，却意外地有人耐读，并且还收到过读者来信:

![](https://raw.githubusercontent.com/guodongxiaren/ImageCache/master/screenshot/reader_letter.jpg)
看完这份邮件，心里也很高兴，虽然我很多事无心插柳（我真的是想好好写技术博客的！），但也真的非常感谢这位网友，我也祝我自己在写作领域能有自己的一番天地吧。


2016年毕业之际，写了一篇又臭又长的博文《写给励志做码农的大学生》，竟然也意外爆红，当时被很多网站和公众号私信授权转载。神奇，所以我真的……文章比代码写的好？


哎，扯远了。

你好，我是果冻虾仁。我是一个话痨，很高兴见到你。


*******************

## 我在这里

|Follow Me|
|---|
|[知 乎][zhihu]
|[微 博][weibo]
|[简书][jianshu]
|[CSDN][csdn]

另外最近在玩公众号，欢迎点赞、关注，分享，转发
![](/img/codepast-banner.png)

*******************
[csdn]:http://blog.csdn.net/guodongxiaren
[zhihu]:https://www.zhihu.com/people/guodongxiaren
[weibo]:http://weibo.com/linpiaochen
[jianshu]:http://www.jianshu.com/u/0c852dd5e473








Template Format
This template can be used to organize your answers to the final project. Items that should be copied from your answers to the quizzes should be given in blue.
Experiment Design
Metric Choice
List which metrics you will use as invariant metrics and evaluation metrics here. (These should be the same metrics you chose in the "Choosing Invariant Metrics" and "Choosing Evaluation Metrics" quizzes.)

For each metric, explain both why you did or did not use it as an invariant metric and why you did or did not use it as an evaluation metric. Also, state what results you will look for in your evaluation metrics in order to launch the experiment.

Measuring Standard Deviation
List the standard deviation of each of your evaluation metrics. (These should be the answers from the "Calculating standard deviation" quiz.)

For each of your evaluation metrics, indicate whether you think the analytic estimate would be comparable to the the empirical variability, or whether you expect them to be different (in which case it might be worth doing an empirical estimate if there is time). Briefly give your reasoning in each case.

Sizing
Number of Samples vs. Power
Indicate whether you will use the Bonferroni correction during your analysis phase, and give the number of pageviews you will need to power you experiment appropriately. (These should be the answers from the "Calculating Number of Pageviews" quiz.)

Duration vs. Exposure
Indicate what fraction of traffic you would divert to this experiment and, given this, how many days you would need to run the experiment. (These should be the answers from the "Choosing Duration and Exposure" quiz.)

Give your reasoning for the fraction you chose to divert. How risky do you think this experiment would be for Udacity?

Experiment Analysis
Sanity Checks
For each of your invariant metrics, give the 95% confidence interval for the value you expect to observe, the actual observed value, and whether the metric passes your sanity check. (These should be the answers from the "Sanity Checks" quiz.)

For any sanity check that did not pass, explain your best guess as to what went wrong based on the day-by-day data. Do not proceed to the rest of the analysis unless all sanity checks pass.

Result Analysis
Effect Size Tests
For each of your evaluation metrics, give a 95% confidence interval around the difference between the experiment and control groups. Indicate whether each metric is statistically and practically significant. (These should be the answers from the "Effect Size Tests" quiz.)

Sign Tests
For each of your evaluation metrics, do a sign test using the day-by-day data, and report the p-value of the sign test and whether the result is statistically significant. (These should be the answers from the "Sign Tests" quiz.)

Summary
State whether you used the Bonferroni correction, and explain why or why not. If there are any discrepancies between the effect size hypothesis tests and the sign tests, describe the discrepancy and why you think it arose.

Recommendation
Make a recommendation and briefly describe your reasoning.

Follow-Up Experiment
Give a high-level description of the follow up experiment you would run, what your hypothesis would be, what metrics you would want to measure, what your unit of diversion would be, and your reasoning for these choices.

