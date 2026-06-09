# 正式自动化任务 Prompt

用途：创建 Codex 每日自动化任务时使用。

任务目标：
每天读取独立 Obsidian 知识库，生成钻石电商图片素材。第一阶段重点是把图片素材关卡做好：批量提示词、提示词去重、生图、AI 自动审核、合格入库、不合格重生或废弃。

路径变量：
- project_root：默认 D:\2026\钻石自动化生图
- kb_root：默认 {{project_root}}\Obsidian-Diamond-Image-KB
- output_root：默认 {{project_root}}\daily-runs\{{date}}

执行前先确认以上路径存在；如果项目路径不同，先按当前电脑实际路径替换变量，不要继续使用写死旧路径。

批量模式：
- preview：2 套
- standard：10 套
- scale：50 套
- bulk：100 套以上

品类比例：
- 钻戒 60%
- 项链 20%
- 耳饰 10%
- 手链 10%

彩钻比例：
- 10 套最多 1 套彩钻。
- 彩钻不得连续出现。
- 最近 10 套窗口内最多 1 套彩钻。
- 彩钻优先用于钻戒，其他品类只低频点缀。

执行规则：
1. 先读取首页、硬规则、产品框架、人物框架、场景框架、拍摄框架、低 AI 味规则、变量抽取策略、自动审核规则。
2. 先批量生成提示词候选，不直接生图。
3. 先计算本批彩钻名额，彩钻不得超过 10%。
4. 审核提示词重复度，剔除或重写重复组合。
5. 每套先从产品 DNA 原型池选择一个完整原型，再生成一个 product_dna。
6. product_dna 必须包含 diamond_color_type 和 colored_diamond_color。
7. product_dna 必须包含 visual_scale_lock 和 supporting_jewelry_limit。
8. 同一套 3 张图必须围绕同一个 product_dna。
9. 每套只抽少量变量，不要把所有词库都塞进提示词。
10. 人物画像围绕年轻网红、时装模特感达人、名媛、富婆、高消费力女性轮换；21-24 岁成人占 75%。
11. 产品可参考高奢珠宝设计语言，但最终提示词不得出现品牌名、Logo、同款、复刻。
12. 场景选定后，动作必须从兼容动作池抽取。
13. 全身图和半身图以人物、穿搭、气质、场景为主，产品只自然出现，不做硬展示。
14. 全身图和半身图中，主产品不能正对镜头、不能居中、不能成为人物动作目的。
15. 彩钻套必须压低其它珠宝存在感，避免强项链、强耳饰、手链、手表抢主彩钻产品。
16. 产品特写必须清楚展示钻石质感、切工、金属反射和合理结构，但要像真实生活局部裁切。
17. 项链特写优先使用 upper outfit crop / neckline styling crop / jewelry resting along neckline 的安全写法。
18. 多数图片使用普通真实拍摄角度，少量穿插时尚杂志化街拍、direct-flash、off-duty model 视角。
19. 正式生成每套输出 3 张独立图，不用三联图作为正式判断。
20. 生图后必须进入图片自动审核。
21. 合格图片进入素材库，不合格图片按规则重生或废弃。
22. 保存图片、product_dna、提示词、评分、索引、失败日志。

每套输出结构：
- set_id
- batch_mode
- category
- diamond_color_type
- colored_diamond_color
- product_dna
- visual_scale_lock
- supporting_jewelry_limit
- design_language_tag
- persona_frame
- age_band
- outfit_frame
- skin_direction
- hairstyle_direction
- makeup_or_expression_direction
- scene_frame
- action_frame
- composition_frame
- lens_frame
- shot_1_full_body
- shot_2_half_body
- shot_3_macro
- negative_rules
- prompt_similarity_check
- image_review_scores
- decision
- saved_files

核心硬限制：
- 不固定人物长相。
- 不复制真实明星、网红、模特或公众人物。
- 不固定场景细节。
- 不固定穿搭细节。
- 只固定 product_dna 和品类比例。
- 彩钻比例固定为最多 10%，10 套最多 1 套。
- product_dna 不能内部矛盾，不能把不同切工、镶嵌、轮廓随机拼接。
- visual_scale_lock 不能在三张图中明显漂移。
- supporting_jewelry_limit 必须被遵守，尤其彩钻套不能让其它珠宝抢主产品。
- colored_diamond_color 必须和 diamond_color_type 一致。
- 不出现品牌名、品牌包装、Logo、同款描述。
- 不要完美磨皮、CGI 感、塑料钻、玻璃假钻、过曝钻石、畸形手指。
- 不要把高消费力女性默认写成成熟外套贵妇。
- 外套造型不能过度集中，10 套最多 4 套；无外套或轻装造型至少 6 套。
- 全身和半身禁止刻意摸戒指、摸项链、举手展示产品、手伸向镜头。
- 全身和半身禁止把主产品正面朝镜头、放在视觉中心或设计成姿势目的。
- 特写不能像僵硬棚拍 packshot。
- 彩钻不能过饱和、发光、像彩色玻璃、像糖果色假钻。
- 特殊角度不能破坏产品可见度、人物自然度和真实感。
- 场景和动作不能冲突，例如餐厅试衣镜、车内走路、运动房拿晚宴酒杯。

镜头硬规则：
- 正常真实视角占 70%-80%。
- 轻微变化视角占 15%-20%。
- 夸张或特殊视角占 5%-10%。
- 如果夸张镜头导致 AI 味变重，优先回退到正常视角。

质量判断：
- 像真实美国高消费力女性会发的照片。
- 画面有钱但不假。
- 人物年轻化、有当代欧美网红或时装模特个性；standard 10 套中 21-24 岁成人至少 8 套。
- 产品真实但不硬广。
- 三张图属于同一 product_dna。
- 三张图遵守同一 visual_scale_lock。
- 彩钻套图中三张图必须保持同一彩钻颜色、切工、金属和镶嵌结构。
- 彩钻套图中其它珠宝不能抢主产品。
- 人物、场景、动作、构图、镜头和产品设计有明显差异。
- 全身/半身以人物和时装氛围为主。
- 特写像真实生活局部，不像棚拍广告图。
- 图片通过自动审核后，才允许进入后续视频生成流程。

审核通过硬门槛：
- 核心维度平均分不低于 8.0。
- 产品一致性不低于 8.5。
- 产品展示自然度不低于 8.5。
- 人物真实感、人物年轻化和个性、动作自然度、低 AI 味均不低于 8.0。
- 商用安全必须通过。

审核输出必须使用固定 JSON 结构，便于后续自动重生和废弃：

```json
{
  "set_id": "",
  "shot_type": "full_body | half_body | macro",
  "scores": {
    "product_consistency": 0,
    "diamond_realism": 0,
    "colored_diamond_realism": null,
    "human_realism": 0,
    "youth_persona": 0,
    "action_naturalness": 0,
    "product_display_naturalness": 0,
    "supporting_jewelry_discipline": 0,
    "visual_scale_consistency": 0,
    "low_ai_feel": 0,
    "composition_usability": 0,
    "video_usability": 0
  },
  "commercial_safety": "pass | fail",
  "hard_fail": false,
  "fail_reason_codes": [],
  "retry_allowed": false,
  "retry_prompt_patch": "",
  "final_decision": "pass | retry | reject"
}
```
