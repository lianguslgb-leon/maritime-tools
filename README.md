# Maritime Tools | 航海工具箱

A bilingual, static maritime reference site designed for mobile and desktop browsers.

中英文双语航海参考工具，适用于手机和电脑浏览器。

## Modules | 功能

1. **Beaufort Wind Converter | 风力换算** (`index.html`): knots, m/s, km/h and Beaufort scale 0–12. Works offline after download.
2. **Tide & Tide Height Predictor | 潮汐与潮高查询** (`tide.html`): official NOAA predictions at 30-minute intervals, chart, high/low water events, daily maximum-minus-minimum range, metres/feet, MLLW datum and port-local time. Previously queried responses are cached in the browser.

## Data availability | 数据覆盖

The initial tide release supports selected U.S. NOAA stations: New York (The Battery), Los Angeles Harbor, Savannah (Fort Pulaski), and San Diego. Other ports are clearly marked as unsupported until a licensed reliable data source is integrated.

首批支持部分美国 NOAA 潮位站：纽约、洛杉矶、萨凡纳、圣迭戈。新加坡、巴生港、鹿特丹、墨尔本等港口尚未接入可靠授权数据源，系统不会虚构预测潮高。

The tide tool requires an internet connection for a first query. Cached results may be viewed again when offline using the same port/date/unit. The Beaufort converter works offline.

首次查询潮汐需要网络；已成功查询的同一港口、日期、单位的数据可在离线时通过再次查询读取缓存。风力换算可离线使用。

## Deployment | 部署

Upload `index.html`, `tide.html`, `README.md` and `LICENSE` to the repository root of the `main` branch. GitHub Pages: Settings → Pages → Deploy from a branch → `main` → `/ (root)`.

将上述文件上传到仓库 `main` 分支根目录，GitHub Pages 设置为从 `main` 分支 `/ (root)` 发布。

## Navigation warning | 航行安全

NOAA tide heights are predicted relative to **MLLW**. The reported daily range is the difference between the maximum and minimum of the day's 30-minute prediction samples; it is not necessarily the range between a particular consecutive HW and LW. Observed levels may differ due to weather. Always check official publications, chart datum and vessel SMS for navigation and UKC decisions.

NOAA 预测潮高基于 **MLLW**。页面的当日潮差为当天30分钟采样数据的最高值减最低值，不一定对应某一对相邻高潮和低潮。实际水位可能受气象影响，航行及富余水深计算须核对官方资料、海图基准和船舶 SMS。

NOAA API: https://api.tidesandcurrents.noaa.gov/api/prod/
