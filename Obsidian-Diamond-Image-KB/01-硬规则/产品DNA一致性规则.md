# 产品 DNA 一致性规则

目标：提高同一套 3 张图的产品一致性，让它们看起来围绕同一个产品，而不是同类产品。

每套必须先生成 product_dna。

product_dna 生成方式：
- 必须先从 [[02-产品框架/产品DNA原型池]] 选择一个完整产品原型。
- 必须先按 [[01-硬规则/彩钻比例规则]] 判断本套是 white diamond 还是 colored diamond。
- 不允许把切工、镶嵌、轮廓、设计语言随机混拼。
- 如果自动化程序需要变化，只能在同一原型内微调金属色、克拉区间、颗粒大小或风格强弱。
- design_language_tag 不得包含另一个不相关切工的形状词，除非明确是 side stones。

product_dna 必填字段：
- category：钻戒、项链、耳饰、手链
- product_role：本套唯一产品主角
- diamond_color_type：white diamond / colored diamond
- colored_diamond_color：无彩钻时为 none；彩钻时从彩钻颜色池选择 1 个颜色
- stone_shape：主石或主要钻石形状
- carat_range：主石大小区间或钻石颗粒规格
- metal_color：金属主色
- setting_type：镶嵌方式
- design_language_tag：设计语言抽象标签
- wearing_area：佩戴部位
- silhouette：产品整体轮廓
- visual_scale_lock：产品在三张图中的视觉大小级别，例：subtle / medium visible / statement but natural
- supporting_jewelry_limit：其它珠宝存在感限制，例：none / minimal / low-profile only
- texture_rules：钻石和金属真实感要求

三张图必须复用：
- category
- diamond_color_type
- colored_diamond_color
- stone_shape
- carat_range
- metal_color
- setting_type
- design_language_tag
- wearing_area
- silhouette
- visual_scale_lock
- supporting_jewelry_limit

允许变化：
- 人物
- 年龄
- 肤色
- 发型
- 服装
- 场景
- 动作
- 镜头
- 构图
- 光线氛围

不允许变化：
- 产品品类变化
- 钻戒变项链或项链变耳饰
- 主石形状明显变化
- 彩钻颜色明显变化
- 金属颜色明显变化
- 镶嵌结构明显变化
- 产品视觉大小级别明显变化，例如全身是小戒指、特写突然变成夸张超大主石
- 其它珠宝抢走本套产品主角位置
- 佩戴部位变化
- 特写图与全身/半身产品不是同一个设计方向
- 产品 DNA 内部自相矛盾，例如切工、镶嵌方式和 silhouette 指向不同产品
- colored_diamond_color 与 diamond_color_type 冲突，例如 white diamond 却写 fancy pink

提示词写法：
- 每张图都引用同一段 product_dna。
- 引用 product_dna 时尽量使用同一段原文，不要每张图重写一遍不同措辞。
- 彩钻只在 product_dna 中低频出现，不要在人物、场景、动作里重复强调。
- 全身图和半身图可以自然露出产品，不硬广。
- 全身图和半身图中，主产品不能正对镜头、不能位于画面视觉中心、不能成为人物动作目的。
- 全身图和半身图中，主产品应像真实随拍里的自然细节：可见但不被摆出来。
- 特写图必须清楚展示产品结构。
- 不为了产品一致性把人物和场景也写死。

现实限制：
- 纯文本生图只能增强一致性，不能保证实拍级完全一致。
- 如果后续需要高度一致，需要加入产品参考图或固定产品素材。
- 当前第一阶段目标是让三张图看起来属于同一套产品方向，先满足内容放量。
