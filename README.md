# pic-bed — Hermes 图床

估值报告 / 选股图表图片仓库（公开，供 Longbridge 长文 / 飞书 / 报告 markdown 引用）。

## 访问方式

- jsDelivr CDN（推荐，国内可访问）:
  `https://cdn.jsdelivr.net/gh/MountainXiu/pic-bed@main/charts/<file>`
- GitHub raw:
  `https://raw.githubusercontent.com/MountainXiu/pic-bed/main/charts/<file>`

## 目录约定

- `charts/` — Ichimoku / K线 / 估值图表，命名 `<SYMBOL>_<type>_<YYYYMMDD>.png`（带日期，避免 CDN 缓存旧版本）

## 上传流程

```bash
cd /work/hermes/pic-bed
cp <本地图> charts/<SYMBOL>_<type>_<YYYYMMDD>.png
git add -A && git commit -m "add <描述>"
git push origin main
```

## 注意

- 仓库必须 Public（Longbridge 抓图 / jsDelivr 均需匿名访问）
- 同名文件更新时请改日期后缀，jsDelivr 缓存约 12h，可用 `https://cdn.jsdelivr.net/gh/...@main/...` 的 purge 接口手动刷新
