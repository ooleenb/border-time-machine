# 国界时间机器 · Border Time Machine

拖动时间轴，看 12 万年来世界版图如何变化。支持平面/地球仪、按宗主国/按政权着色、中英双语、政权搜索。

Drag the timeline to watch 120,000 years of world borders change. Flat/globe views, colour by sovereign or polity, Chinese/English, polity search.

## 本地运行 / Run locally

```bash
python3 -m http.server 8000
# 打开 http://localhost:8000
```

不能直接双击 `index.html`：页面用 `fetch` 读取 `data/`，`file://` 下会被浏览器拦截。

## 结构 / Structure

- `index.html` — 页面（D3.js + topojson-client，从 jsDelivr CDN 加载）
- `data/world_*.json` — 54 个年份的边界（TopoJSON，已简化）
- `data/index.json` — 年份列表与政权索引
- `data/zh.json` — 政权中文名对照
- `data/land.json` — 海陆底图（Natural Earth，via world-atlas）

## 数据与许可 / Data & licence

边界数据来自 [aourednik/historical-basemaps](https://github.com/aourednik/historical-basemaps)（GPL-3.0），本项目对其做了简化和格式转换，因此整体按 GPL-3.0 发布，见 `LICENSE`。边界为近似复原，不宜作学术引用。
