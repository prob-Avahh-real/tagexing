# 踏歌行

踏歌行游戏化。Canvas 物理引擎 + 手绘赛道 + 节奏同步。

## 平台

| 平台 | 方式 |
|------|------|
| iOS / Android | Capacitor |
| 手表 | 窄屏 CSS |
| 智能戒指 | 倾斜切歌 / 大幅倾斜撤销 |
| 智能手杖 | 轻点播放暂停 / 摆动清空 |

## 技术

- Canvas 2D 绘制 + 物理碰撞
- Web Audio 节奏同步
- Capacitor 原生包装
- DeviceOrientation / DeviceMotion

## 构建

```bash
npm install
npm run build          # 同步 www/
npx cap sync
```

## Harness / Loop（助手）

- 遵循根 `/Users/skat/AGENTS.md`：**Harness Engineering** + **Loop Engineering**
- Guide = 本文件；Sensor = 下方验证命令；同类失误第二次须沉淀规则或测试（棘轮）
- 开干前写清 **Done**；每切片过验证环；显式停止（成功 / 上限 / 无进展 / 人审）
- 详解：`docs/HARNESS_ENGINEERING.md`、`docs/LOOP_ENGINEERING.md`

## 验证环 / Done

```bash
npm install
npm test          # 若有
npm run build     # 或 build:web
npx cap sync android   # 若有 android/
# 可选：JAVA_HOME=…/openjdk@17 npm run apk:debug
```

**Done 示例**：测试通过（若有）+ web 产物进 `www/`/`dist/` + `cap sync` 无报错。可选穿戴未做可搁置，不纳入强制 Done。
