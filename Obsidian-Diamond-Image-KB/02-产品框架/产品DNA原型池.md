# 产品 DNA 原型池

用途：放量生成时先选一个完整产品原型，再生成 product_dna。不要把切工、镶嵌、轮廓和设计语言随机混拼。

核心规则：
- 每套先从本文件选 1 个产品原型。
- product_dna 必须保持内部一致。
- product_dna 必须包含 diamond_color_type 和 colored_diamond_color。
- product_dna 必须包含 visual_scale_lock 和 supporting_jewelry_limit。
- design_language_tag 不能出现另一个不相关切工的形状词。
- 如需变化，只允许在同一原型内微调金属色、克拉区间、颗粒大小或风格强弱。
- 三张图必须复用同一段 product_dna 原文。
- 三张图必须遵守同一 visual_scale_lock，不能让同一产品忽大忽小。
- 彩钻原型按 [[01-硬规则/彩钻比例规则]] 低频使用。

不允许的组合：
- round-cut + emerald-cut architecture
- marquise-cut + cushion softness
- pear-cut + princess geometry
- cushion-cut + oval silhouette
- tennis necklace + pendant silhouette
- stud earrings + drop earring silhouette
- tennis bracelet + cuff silhouette

允许的表达：
- emerald-cut center stone with tapered baguette side stones
- oval center stone with hidden halo and slim pave band
- pear-shaped center stone with delicate halo
- round solitaire pendant on a fine chain
- graduated tennis necklace resting on collarbone

## 彩钻原型规则

彩钻颜色池：
- fancy yellow
- champagne
- fancy pink
- light blue
- cognac
- soft green

彩钻使用原则：
- 默认优先用于大克拉钻戒。
- 项链、耳饰、手链只做低频点缀。
- 彩钻颜色必须克制、真实、有自然折射。
- 不允许过饱和、糖果色、发光宝石感、彩色玻璃感。
- 彩钻套 supporting_jewelry_limit 默认 minimal or none。
- 彩钻套全身/半身禁止强项链、强耳饰、多层手链、手表抢主彩钻产品。

## visual_scale_lock 默认规则

只允许使用以下 3 个枚举值：
- subtle
- medium visible
- statement but natural

- 大克拉钻戒：statement but natural
- 普通钻戒：medium visible
- 彩钻钻戒：statement but natural
- 经典项链：medium visible
- 细链或叠戴项链：subtle
- 耳饰：medium visible
- 手链：medium visible

## supporting_jewelry_limit 默认规则

- 白钻钻戒：low-profile only
- 彩钻钻戒：minimal or none
- 项链：minimal earrings allowed, no competing necklace, no statement earrings
- 耳饰：no competing statement necklace, necklace must be absent or very subtle
- 手链：low-profile rings allowed, no competing bracelet stack, watch must not dominate

## 钻戒原型

- round brilliant solitaire, 2-4ct, platinum or white gold, six-prong setting, clean elevated solitaire, finger, balanced round center-stone profile
- oval hidden halo ring, 3-5ct, platinum or yellow gold, hidden halo with slim pave band, elongated oval elegance, finger, soft elongated profile
- emerald-cut three-stone ring, 3-6ct, platinum, tapered baguette side stones, architectural step-cut clarity, finger, clean rectangular profile
- cushion halo ring, 4-7ct, white gold or rose gold, delicate halo with pave band, soft cushion statement, finger, cushion-shaped profile
- pear-shaped cathedral ring, 3-5ct, platinum or yellow gold, cathedral setting with fine pave, romantic pear-shaped elegance, finger, teardrop profile
- radiant-cut pave ring, 4-8ct, white gold, pave band with clean prongs, modern radiant sparkle, finger, crisp rectangular profile
- marquise bezel ring, 2-4ct, yellow gold or platinum, slim bezel or half-bezel setting, vintage marquise line, finger, pointed elongated profile
- princess-cut channel ring, 2-4ct, white gold, channel-set accent band, clean geometric princess style, finger, square center-stone profile

## 彩钻钻戒原型

- fancy yellow oval ring, 4-7ct, platinum or yellow gold, hidden halo or slim pave band, warm high-jewelry statement, finger, elongated oval colored-diamond profile
- champagne cushion ring, 4-7ct, rose gold or yellow gold, delicate halo with pave band, soft warm cushion statement, finger, cushion-shaped colored-diamond profile
- fancy pink pear-shaped ring, 3-5ct, platinum or rose gold, fine halo or cathedral setting, romantic rare-color elegance, finger, teardrop colored-diamond profile
- light blue emerald-cut ring, 3-5ct, platinum, clean bezel or tapered side stones, cool architectural colored-diamond clarity, finger, clean rectangular colored-diamond profile
- cognac radiant-cut ring, 4-8ct, yellow gold, pave band with clean prongs, rich warm radiant sparkle, finger, crisp rectangular colored-diamond profile

## 项链原型

- round solitaire pendant, medium visible scale, platinum or yellow gold, simple four-prong pendant, classic everyday luxury, neck / collarbone, centered pendant silhouette
- graduated tennis necklace, fine to statement scale, white gold or platinum, continuous prong-set diamonds, red carpet classic line, neck / collarbone, smooth collarbone curve
- station diamond necklace, delicate to medium scale, yellow gold or rose gold, bezel or prong-set stations, relaxed wealthy layering, neck / collarbone, airy chain silhouette
- emerald-cut pendant necklace, medium visible scale, platinum, clean bezel or four-prong setting, architectural pendant clarity, neck / collarbone, slim rectangular pendant silhouette
- pear-shaped drop pendant, medium visible scale, white gold or yellow gold, fine prong setting, soft evening elegance, neck / collarbone, teardrop pendant silhouette
- layered delicate diamond necklace, subtle sparkle scale, yellow gold or white gold, small bezel-set diamonds, modern influencer layering, neck / collarbone, layered fine-chain silhouette

## 彩钻项链原型

- fancy yellow solitaire pendant, medium visible scale, yellow gold or platinum, simple four-prong pendant, understated colored-diamond accent, neck / collarbone, centered colored pendant silhouette
- champagne station necklace, delicate to medium scale, yellow gold or rose gold, bezel-set colored diamond stations, relaxed warm luxury layering, neck / collarbone, airy colored station silhouette

## 耳饰原型

- round diamond stud earrings, medium visible scale, platinum or white gold, classic prong setting, clean everyday luxury, ears / earlobe, round stud silhouette
- cushion halo stud earrings, medium visible scale, white gold or rose gold, delicate halo setting, soft evening sparkle, ears / earlobe, cushion-shaped stud silhouette
- diamond huggie hoops, small to medium scale, yellow gold or white gold, pave-set front face, modern socialite casual luxury, ears / earlobe, minimal hoop outline
- pear-shaped drop earrings, medium to statement scale, platinum or yellow gold, prong-set drop, romantic event jewelry, ears / earlobe, soft vertical drop silhouette
- emerald-cut drop earrings, medium to statement scale, platinum, step-cut stones with clean links, architectural evening style, ears / earlobe, slim vertical rectangular silhouette
- diamond ear climbers, small to medium scale, white gold, graduated prong-set stones, young influencer edge, ears / earlobe, upward ear-line silhouette

## 彩钻耳饰原型

- fancy yellow diamond studs, medium visible scale, yellow gold or platinum, classic prong setting, warm colored-diamond everyday luxury, ears / earlobe, round colored stud silhouette
- fancy pink drop earrings, medium visible scale, rose gold or platinum, prong-set drop earrings, romantic low-frequency colored accent, ears / earlobe, soft vertical colored drop silhouette

## 手链原型

- classic tennis bracelet, medium diamond scale, white gold or platinum, continuous prong setting, timeless wealthy staple, wrist, flexible line bracelet silhouette
- bezel-set diamond station bracelet, delicate to medium scale, yellow gold or rose gold, bezel stations on fine chain, relaxed everyday luxury, wrist, airy chain silhouette
- diamond bangle bracelet, medium visible scale, yellow gold or white gold, pave-set top face, polished affluent minimalism, wrist, structured bangle silhouette
- emerald-cut line bracelet, medium to statement scale, platinum, repeating step-cut stones, architectural high-jewelry feel, wrist, clean rectangular line silhouette
- mixed diamond tennis bracelet, medium visible scale, white gold, alternating round and baguette stones, modern classic variation, wrist, refined line bracelet silhouette
- delicate layered diamond bracelet, subtle sparkle scale, yellow gold or rose gold, small prong-set stones with fine chain, influencer stacking style, wrist, layered fine-chain silhouette

## 彩钻手链原型

- champagne diamond station bracelet, delicate to medium scale, yellow gold or rose gold, bezel-set colored diamond stations, low-frequency warm accent, wrist, airy colored station silhouette
