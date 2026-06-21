# 生图提示词模板

## 🚨 核心策略：图生图优先

**所有小工配图必须使用图生图（image-to-image），以参考图作为底图输入，确保形象一致。**

参考底图路径：`assets/reference/xiaogong-front.png`

---

## 图生图 Prompt 模板

```bash
python {baseDir}/scripts/generate_image.py \
  --prompt "Same exact character — preserve every detail of face, glasses, hair, skin tone, clothing, art style, body proportions. Only change the pose and scene. {场景描述}" \
  --filename "output.jpg" \
  -i "assets/reference/xiaogong-front.png" \
  --aspect-ratio 16:9
```

### 场景 Prompt 填充模板

```text
Same exact character — preserve every detail of face, glasses frame thickness, dark brown side-parted quiff hair with lighter highlights, medium black rectangular glasses, warm peach skin tone, large round eyes, small round ears, dark grey-blue collared long-sleeve shirt (#4B5868) optionally with sleeves rolled up, dark charcoal trousers (#383C42), clean digital cel-shading art style with medium-weight black outlines, approximately 3.5 heads tall chibi proportion.

IMPORTANT: The character should be relatively small in the composition — no more than 30% of image height and 20% of image width. The diagram/structure/workflow should be the main visual content. The character stands beside the content, pointing or explaining, not dominating the frame.

Only change: the pose and environment. Now the character is {场景描述}.

Pure white background. Keep everything else identical to the original.
```

---

## 服装体系切换

### 体系A — 日常办公工装（室内/软件场景）

参考底图自带深灰蓝衬衫，无需切换。

### 体系B — 防静电无尘工作服（工厂/硬件/现场调试）

当需要现场工作服时，增加服装描述：

```text
Same exact character — but change the clothing to: full-body light sky-blue static-free jumpsuit (#94C6E8), lapel collar, elastic cuffs, clean utility cut, no logos, matching light blue static-free trousers. Keep face, glasses, hair, skin, ears, art style exactly the same.
```

---

## 文生图方案（仅在无参考底图时使用）

### 基础通用正向关键词

```text
Q版卡通男生，约3.5头身，干净数字cel-shading插画，中等粗细黑色轮廓线，平涂柔和低饱和色彩，硬边阴影，纯白色背景，无渐变，无写实质感
```

### 角色锁定关键词

```text
年轻男生，深棕色短侧分上翻短发(quiff风格)，头顶蓬松，两侧修剪利落，浅棕色高光纹理。黑色中框方眼镜(框厚约占镜片1/5~1/6)，镜框圆角，镜片透明。暖桃肤色(#FFF0D5)，圆润Q版脸蛋。大圆眼(接近正圆)，深棕虹膜+白色圆形反光点，细淡眉毛，小巧薄唇，耳朵中等偏小巧圆润。
```

### 画风禁止负面关键词

```text
写实，3D，厚涂，浓阴影，渐变，复杂纹理，五官变形，换发型，去掉眼镜，尖脸，长脸，高饱和色彩，真人照片，二次元美型脸，手绘蜡笔，铅笔纹理，细框眼镜，粗框眼镜，纯黑头发，冷白肤色，杏仁眼，夸张大圆眼，大耳朵，极端2头身，标准7头身
```

---

## 文生图完整英文模板（备选）

每张图单独生成。替换 `{变量}`。

```text
Generate one standalone 16:9 horizontal Chinese article illustration.

Style:
Clean digital cel-shading. Medium-weight black outlines. Flat solid colors with hard-edged shadows, low-saturation muted palette. No gradients, no realistic shadows, no textures, no brush strokes. Pure white background.

Character:
小工, a Q版 chibi male engineer, ~3.5 heads tall. Dark brown side-parted quiff hair (#3B332D) with lighter highlights, neat sides. Black medium-thickness rectangular glasses (frame ~1/5 to 1/6 of lens height). Large round eyes (nearly circular), dark brown irises with white catchlights. Thin light eyebrows, small thin lips, gentle expression. Small round ears. Warm peach skin (#FFF0D5). Soft round face.

Clothing: {服装体系A或B}

Theme: {正文配图主题}
Structure type: {结构类型}
Core idea: {核心意思}
Composition: {具体画面}
Suggested elements: {元素列表}
Chinese labels: {标注词列表}

Color rules:
Black outlines + glasses. Hair dark brown #3B332D (not black). Skin warm peach #FFF0D5. Shirt dark grey-blue #4B5868 or jumpsuit light sky-blue #94C6E8. Orange for flow/arrows. Red for warnings/results. Blue for secondary notes.

Constraints:
One core structure per image. Subject 40-60% of canvas. ≥35% white space. 5-8 short Chinese labels max. No title in top-left. No structure type on image. No formal diagram. Fresh composition each time.
```

---

## 图像编辑提示

### 去掉左上角标题

```text
Edit the provided image. Remove only the title "{要删除的文字}" and its underline from the top-left corner. Fill that area with the same clean white background. Preserve everything else exactly. Do not add new text or objects.
```

### 增强小工参与度

```text
Same exact character. Make 小工 more central to the action — doing the work that explains the idea: debugging, measuring, building, pointing at key details, or presenting a result. Not standing beside the diagram. Clean digital cel-shading, flat colors.
```
