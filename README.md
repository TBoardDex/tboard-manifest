# TBoard SDK Download

## Development

```bash
mkdir -p tboard
cd tboard
repo init -u https://github.com/TBoardDex/tboard-manifest.git -b master -m development.xml
repo sync -j4
```

## Linux 5.10 (branch-pinned)

与 `development.xml` 相同的组件版本，但共用仓库（`device/rockchip`、`rkbin`、`tools`、`u-boot`、`repo`）固定到 `linux-5.10` 分支，便于与后续 6.12 SDK 在同一仓库内并行演进：

```bash
mkdir -p tboard-linux-5.10
cd tboard-linux-5.10
repo init -u https://github.com/TBoardDex/tboard-manifest.git -b master -m linux-5.10.xml
repo sync -j4
```

## v1.0.0

Download all components at their `v1.0.0` tags:

```bash
mkdir -p tboard-v1.0.0
cd tboard-v1.0.0
repo init -u https://github.com/TBoardDex/tboard-manifest.git -b master -m v1.0.0.xml
repo sync -j4
```

## Release Firmware

固件下载地址：https://github.com/TBoardDex/tboard-manifest/releases
