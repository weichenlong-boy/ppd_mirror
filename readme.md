## 数据情况

| 表名 | 内容 | 备注 |
| ------ | ------ | ------ |
| train | 训练集 |  |
| test | 测试集 |  |
| listing_info | 标的属性 |  |
| user_info | 用户信息 |  |
| user_taglist | 用户画像 |  |
| user_behavior_logs | 用户行为SDK |  |
| user_repay_logs | 还款日志 |  |

##特征工程

###Y
* 多分类问题 未还款-1 还款0~31
* 多分类问题 未还款-1 /当天还款 一/ 1 2 3二/4 5 6 7三/8 9 10 11 四/12 13 14 15五/
16 17 18 19六/20 21 22 23七/24 25 26 27 八/28 29 30 31 九
* 多分类问题 未还款/当天还款/提前还款
* 二分类问题 是否在账单日还款
* 二分类问题 是否逾期
### train/test
* 近3月订单数
* 近3月订单金额最大值
* 近3月订单金额均值
* 近3个月提前还款日期均值
* 近3个月提前还款日期最小值
* 近3个月提前还款日期最大值
* 近6月订单数
* 近6月订单数金额最大值
* 近6月订单金额均值
* 近6个月提前还款日期均值
* 近6个月提前还款日期最小值
* 近6个月提前还款日期最大值
* 是否有首逾记录

### listing_info
* 用户当前标的属性（期数，费率，总金额）
* 用户近3个月标的期数均值、最大值、最小值
* 用户近3个月标的费率均值、最大值、最小值
* 用户近3个月标的总金额均值、最大值、最小值
* 用户近6个月标的期数均值、最大值、最小值
* 用户近6个月标的费率均值、最大值、最小值
* 用户近6个月标的总金额均值、最大值、最小值
* 用户近9个月标的期数均值、最大值、最小值
* 用户近9个月标的费率均值、最大值、最小值
* 用户近9个月标的总金额均值、最大值、最小值
* 用户近12个月标的期数均值、最大值、最小值
* 用户近12个月标的费率均值、最大值、最小值
* 用户近12个月标的总金额均值、最大值、最小值
* 历史借款距当前最小天/最大天

### user_info
* 性别、年龄、身份证省、id省
* 身份证和id是否同一个省
* 注册时间据放款时间的月数

### user_taglist 
* 多少个不同的用户画像

### user_behavior_logs
* 用户近7天行为数
* 用户近7天行为1数、2数、3数
* 用户近15天行为数
* 用户近15天行为1数、2数、3数
* 用户贷款当天行为数
* 用户当天行为1数、2数、3数
* 用户贷款当天白天行为数8~22点
* 用户贷款当天夜间行为数22~8点
* 用户0~31天行为


### user_repay_logs
* 用户历史所有订单还款平均时间，若平均时间逾期则不还钱概率大，若平均时间超过一个月则算作工作日还款，
若平均时间在一月以内则认为是发工资日还款
* 平均还款时间
* 历史逾期次数
* 历史订单数
* 历史1期账单还款时间
* 历史2期账单还款时间
* 历史3期账单还款时间
* 最近一次账单还款时间


