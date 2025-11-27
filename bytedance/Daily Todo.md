# 2025年09月18日

需求-视频锚点召回

- [x] check list review ⏫ ✅ 2025-09-18
- [ ] destination url 簇 召回 
	- [x] 已同步 ✅ 2025-09-18
- [ ] 自测联调 🔼 



# 2025年09月22日
需求-视频锚点召回
- [ ] 对齐destination url和锚点url match方式
- [ ] 实现新方式的代码和自测

需求-ad-site-i18n-sg bucket 切私
- 时间 下周一上
- 文档 https://bytedance.sg.larkoffice.com/docx/GZhddE6hSoOrrVxTebalqfAfgtg
- [ ] 技术方案调研
	- 梳理调用流程
	- Tool-图片素材统计
		- images 把 image-url 补充上
		- Interactive Add-on 从 preview_info 查询对应的 url 补充上 preview_info_url字段



# 2025年09月25日
需求-视频锚点召回
- [x] bff 代码 mr https://code.byted.org/ad/tt4b_creation_bff/merge_requests/1170?dv_filepath=biz%2Fmodel%2Fad%2Fsco%2Fsmart_creative%2Fsmart_creative.go&to_version=9 ✅ 2025-09-26
- [x] garm 代码 mr https://bits.bytedance.net/code/ad/ad_garm/merge_requests/1533 ✅ 2025-09-26
- [x] gre 代码 mr  https://code.byted.org/adgrowth/growth_algorithm/merge_requests/326?dv_filepath=plugin%2Fbusiness%2Fttam_creative%2Fadditional_channel_rerank.go ✅ 2025-09-28
	- [ ] 确定gre 的火车集成完后，预发环境是不是 ppe_i18n_platform
- [ ] 发布📅 2025-09-29 


需求-ad-site-i18n-sg bucket 切私
- [x] 联调完毕 ✅ 2025-09-25
- [x] lego_common mr i18n分支 https://code.byted.org/ad/lego_common/merge_requests/406 ✅ 2025-09-25
- [x] lego_creative cr ✅ 2025-09-28
	- [x] 已通过 ✅ 2025-09-26
	- [ ] 代码合并
- [x] lego_creative 发布 📅 2025-09-28 ✅ 2025-09-28
- tce https://cloud-i18n.bytedance.net/tce/services/7813?module=ticketList&x-resource-account=i18n&x-bc-region-id=bytedance
- tce升级单 https://cloud-i18n.bytedance.net/tce/deployment_new/522865016?current_stage_id=6964189444&service_id=7813&x-bc-region-id=bytedance&x-resource-account=i18n

lego-ttam 核心接口梳理


# 2025年10月09日

- [x] 白名单放量 ✅ 2025-10-09
	- 技术侧放量
		- alpha和beta阶段 圈选出一些功能有效的目标adv id去配置。数量级也几十个、几百个左右。时间几天，可以根据功能的影响去变动。
		- 如果无客诉，可以进行百分比放量。5%、10%、20%这样每个阶段观察一两天左右，如无问题后续放量可以以 60%、80%直至100% 
- [x] lego oncall ✅ 2025-10-09



# 2025年10月13日

- [x] 锚点召回放量5% ✅ 2025-10-15
- [x] lego 代码 ✅ 2025-10-16
- [x] oncall 报警 ✅ 2025-10-16

## 2025年10月15日
- [x] 锚点召回放量20% ✅ 2025-10-15
- [x] lego 代码 ✅ 2025-10-16
- [x] oncall 报警 ✅ 2025-10-16





- [x] 审核链路的素材put流程排查 ✅ 2025-10-16

- [x] tt_ads接口安全工单 ✅ 2025-10-22
	- [x] get_video_posters、get_cover_uri 两个接口加开关 material_permission_check_config 观察指标 ad.platform.tt_ads.check_material_permission ✅ 2025-10-20
		- [x] bytediff ✅ 2025-10-20
		- [x] 发布单 ✅ 2025-10-20
	https://cloud-i18n.bytedance.net/tcc/detail/5508/config?x-resource-account=i18n&x-bc-region-id=bytedance&env=prod&region=MVAALI&confspace=default
		- [ ]  放量节奏
			- 22号 10% 24号 50 % 27号100%
	- [ ] get_video_meta_info 接口跟进前端下线。
- [x] 锚点 放量百分之40% ✅ 2025-10-20


## DEV
- [x] creation rpc panic @lz ⏳ 2025-10-28 ✅ 2025-10-28
流程
```plaintext
UpdateCreative（handler.go:70）
→ CreativeAppSrv.UpdateCreative（creative_write_srv.go:167）
→ 执行创意构建工作流（创建DB模型）
→ CreativeEntityToDB（creative_repo.go:60）
→ SmartPlusPlusTemplateEntityToDB（media_list.go:436）
→ ConvertToMediaModel（media.go:672）
→ ConvertToMediaModelByCarousel（media.go:681）
→ BuildImageInfoModels（media.go:175）→ 触发panic
```

- [x] creator ac @xy ⏳ 2025-10-31 ✅ 2025-10-28
问题:
1. 原生推、原生拉

## oncall
- [x] creative_platorm_rpc_i18n 分页查询缺少某一素材 可用vid查询 ✅ 2025-10-22

## 工单
- [x] lego_core db 扩容 ✅ 2025-10-28






### 2025年10月28日
- [x] material_name 加上后的验证 ✅ 2025-10-29
- [ ] AIGC渠道的Auto_pull的改动
	- aigc 召回加上 compain id (input_params)
	- ac增补的场景调用 aigc 透传参数 （input_params)

 - ac增补的 aigc不要过滤历史 history的 aigc素材 (AIGCVideoHistoryFilter 里做判断逻辑)
 - ac增补的  history_provider  过滤掉 aigc素材 (新增filter然后 通过 placement_id 来判断 ?)


## 2025年10月30日
AIGC渠道的Auto_pull的改动
1. 和振健、慧斌确定方案









- [x] gre event 恢复 ✅ 2025-11-11


明日计划
- [x] 封板结束后改QueryMusics的限流 提升到300 ✅ 2025-11-14

- [ ] redis集群下线
- [ ] lego_business overpass建立
- [ ] binlog 构建新的faas服务









1. 
2.  material_ref upsert 逻辑再确认一下
