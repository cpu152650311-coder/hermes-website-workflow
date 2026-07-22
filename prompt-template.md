# 建站 Prompt 模板

> 复制以下内容，把 `{ }` 占位符替换为实际值后使用。
> 此模板会覆盖 v11 中的电子制造默认值，强制 Agent 基于你的行业重新设计。

---

## 使用方式

发送以下全部内容作为建站指令（替换所有 `{...}` 占位符）：

```
## 建站任务

**行业/品类**：{你做什么，例如：LED lighting, lithium batteries, injection molding...}
**品牌名**：{品牌名，例如：RayLux}
**语言**：{英文站选 en，中英双语选 zh+en}
**部署域名**：{最终域名，例如：raylux-led.com}

## ⛔ 行业重置指令（最高优先级）

这是一个 **{你的行业}** 站点，**不是 PCB/PCBA/电子制造**。

**强制禁止**：
- 禁止使用 PCB 相关的产品参数（层数/线宽线距/阻抗/沉金/OSP/FR-4/罗杰斯/铝基/陶瓷基）
- 禁止使用 SMT/PCBA 相关的工艺描述（贴片/回流焊/波峰焊/AOI/飞针测试）
- 禁止使用电子制造的认证体系（UL/IATF 16949/IPC 标准——除非这些真的适用）
- 禁止使用 `{Brand Name} | Professional PCB Manufacturing` 这类 title 格式
- 禁止从 huaxingpcba.com 的设计模式复制（暗金配色、PCB 纹理、电路板意象）
- phase 0 的"填充策略"表格是电子制造专用的，**忽略它**，改用下面这行：

  **此站自动填充策略**：{一句话说明你的行业的标准字段，例如："LED行业按光效/色温/CRI/光束角/防护等级/LM-80 展开" 或 "注塑行业按吨位/材料/模具类型/公差/表面处理/最小批量 展开"}

## ⛔ 设计重置指令（最高优先级）

- 禁止使用 huaxingpcba 的暗金(#c8963e)配色
- 禁止使用电子制造相关的视觉意象（电路/芯片/焊点/PCB 走线/绿油）
- 重新走 Phase 1 的**品类细分 → 品牌人格三轴 → 差异化**流程，基于 {你的行业} 选择视觉方向
- 页面骨架模式只是结构参考（Hero→Trust→Split→CTA），**不是视觉参考**
- CTA 按钮文字基于你的行业改写（不是 "Get PCB Quote"），例如：
  {根据你的行业给出 2-3 个合适的 CTA 文案，例如 "Get Free Sample" / "Request Lighting Plan"}

## ⛔ 能力页面树重置

当前 SKILL.md 的能力页展开示例全是 PCB/PCBA/SMT，**全部忽略**。
根据你的行业，能力页应该是：
{列出你的行业的能力分类，例如：
- capabilities/led-components/{smd-led, high-power, cob, filaments}
- capabilities/custom-solutions/{spectrum-tuning, waterproofing, smart-control}
- capabilities/manufacturing/{die-bonding, phosphor-coating, binning-testing}
}

## 站点完成度标准

基于 v11 要求（除了博客只需 3 篇）：
- ✅ 核心信任页全部创建（about, factory, quality, shipping, faq, how-it-works, design-guides, privacy, terms, 404）
- ✅ 能力页按上面定义展开（至少 2 层深度）
- ✅ 行业应用页（{列出你的典型应用行业，例如：commercial, industrial, horticulture, automotive, residential}）
- ✅ 每页 SEO：独立 title/description + og:tags + canonical + JSON-LD
- ✅ 安全头 + robots.txt + sitemap.xml + llms.txt
- ✅ 表单：inquiry-proxy.workers.dev，3-4 字段
- ✅ 图片：全 low 质量，零复用，50-80 张
- ✅ Google Ads 落地页 /welcome/
- ✅ 博客框架（/blog/index.html，文章由 blog-workflow 后续生成 3 篇）

## 设计差异化要求

请主动做以下差异化决策（在 design-blueprint.md 中记录）：
- [ ] 主色：不选电子制造常用的深绿/金/铜，选你行业的标志色
- [ ] Hero 构图：不选 PCB 微距/车间广角，选你行业的视觉母题
- [ ] 字体个性：与 huaxingpcba 的 mono+serif 组合不同
- [ ] 布局密度：与 huaxingpcba 的密集信息风格形成对比
- [ ] CTA 策略：不只用弹窗，考虑其他形式
- [ ] 图片风格：不做电子产品微距摄影，做你行业的视觉语言

---

开始建站。
```
