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

- [ ] tt_ads接口安全工单
	- [x] get_video_posters、get_cover_uri 两个接口加开关 material_permission_check_config 观察指标 ad.platform.tt_ads.check_material_permission ✅ 2025-10-20
		- [x] bytediff ✅ 2025-10-20
		- [x] 发布单 ✅ 2025-10-20
	https://cloud-i18n.bytedance.net/tcc/detail/5508/config?x-resource-account=i18n&x-bc-region-id=bytedance&env=prod&region=MVAALI&confspace=default
	- [ ] get_video_meta_info 接口跟进前端下线。
- [x] 锚点 放量百分之40% ✅ 2025-10-20


dev
- [ ] creation rpc panic @lz
- [ ] creator ac @xy

oncall
- [ ] creative_platorm_rpc_i18n 分页查询缺少某一素材 可用vid查询