
心得体会
测试的log.info不能带上线，开发环境验证后立即删除\

今日工作
- [FD-276549](http://pmo.corp.qunar.com/browse/FD-276549) 推广员项目推广活动页策略迭代
    - - 自测中，梳理创建流程，查看活动创建记录的入库流程。

明日计划
1. 自测创建活动、身份打标、绑定和助力环节的数据入库情况。
2. mock出各种情况的酒店订单，执行返现测试。




今日工作
 - 对齐小程序我的页面发布步骤和准备线上配置
 - 推广员项目自测推进，目前进行到标签打标部分


明日计划
小程序我的页面发布
推广员项目绑定流程自测完毕。


今日工作
- 小程序项目发布

明日计划
接口接入灭霸
接口写到文档里


	noah本地化插件，环境不能重名，即便环境已经被销毁。

今日工作
- [FD-276549](http://pmo.corp.qunar.com/browse/FD-276549) 推广员项目推广活动页策略迭代 自测中
	- 修复了若干个导致绑定和奖励记录无法入口的bug
	- 接受酒店离店消息判断身份执行返现自测 70% 预计明天能完成自测

额外改动
1. sc_b_bind_record表添加字段 record_no
2. rebate_reward_streategy.t配置设置 crowUserName为ALL
3. 改变分组不再是默认为true，而是依据拉新拉活的标签进行判断
4. 修改绑定 BaseBindCommonPreCheckExt 的 wx_promotion_binding_group分组校验不通过时 发放奖励extcode: newOldAvailableBoostLabel 为 oldUserAvailableBoostLabel