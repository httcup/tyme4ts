# Tyme [![License](https://img.shields.io/badge/license-MIT-4EB1BA.svg?style=flat-square)](https://github.com/6tail/tyme4ts/blob/master/LICENSE)

Tyme是一个非常强大的日历工具库，可以看作 [Lunar](https://6tail.cn/calendar/api.html "https://6tail.cn/calendar/api.html") 的升级版，拥有更优的设计和扩展性，支持公历、农历、藏历、回历、星座、干支、生肖、节气、月相、法定假日等。

## 在线演示

本项目在本仓库的 `docs/` 目录附带演示站点，构建时用 esbuild 将 `lib/index.ts` 打包为浏览器可用的 `tyme.min.js`：

- `docs/index.html` 万年历：公历 / 农历 / 干支 / 节气 / 月相 / 神煞宜忌 / 八字排盘 / 月历
- `docs/query.html` 日期查询：公历 ↔ 农历双向换算、四柱（含时柱）、纳音、星宿值神、冲煞、下一节气时刻、传统黄历全文


- GitHub Pages：https://httcup.github.io/tyme4ts/
- Cloudflare Pages：https://tyme4ts.pages.dev/

## 示例

    // install
    npm init -y
    npm i typescript -D
    npm i ts-node -D
    npm i tyme4ts
     
    // test.ts
    import {SolarDay} from 'tyme4ts';
     
    const solar: SolarDay = SolarDay.fromYmd(1986, 5, 29);
     
    // 1986年5月29日
    console.log(solar.toString());
     
    // 农历丙寅年四月廿一
    console.log(solar.getLunarDay().toString());
     
    // 第十七饶迥火虎年四月廿一
    console.log(solar.getRabByungDay().toString());
     
    // 1406年赖买丹月20日
    console.log(solar.getHijriDay().toString());
     
    // run
    ts-node test.ts

## 文档

请移步至 [https://6tail.cn/tyme.html](https://6tail.cn/tyme.html "https://6tail.cn/tyme.html")

## Star History

[![Star History Chart](https://star-history.dera.page/svg?repos=6tail/tyme4ts&type=Date)](https://star-history.dera.page/#6tail/tyme4ts&Date)

## 致谢
1. 感谢许剑伟老师分享的寿星天文历，本项目节气算法引自 [https://github.com/sxwnl/sxwnl](https://github.com/sxwnl/sxwnl "https://github.com/sxwnl/sxwnl")
2. 感谢[stonelf](https://github.com/stonelf "https://github.com/stonelf")，本项目藏历数据引自 [https://github.com/stonelf/zangli](https://github.com/stonelf/zangli "https://github.com/stonelf/zangli")
