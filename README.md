# TBoard SDK Download

## Development

```bash
mkdir -p tboard
cd tboard
repo init -u https://github.com/TBoardDex/tboard-manifest.git -b master -m development.xml
repo sync -j4
```

## Linux 6.12 (RK3588/RK3588S, Debian 13 / Ubuntu 24.04)

新一代 SDK：kernel 6.12、U-Boot 2025.04、Debian 13 (Trixie)、Ubuntu 24.04。共用仓库（`device/rockchip`、`rkbin`、`tools`、`u-boot`）固定到 `linux-6.12` 分支，kernel 以 `path="kernel"` 检出（本地目录名为 `kernel`，源仓库为 `rockchip-kernel-6.12`）：

```bash
mkdir -p tboard-linux-6.12
cd tboard-linux-6.12
repo init -u https://github.com/TBoardDex/tboard-manifest.git -b master -m linux-6.12.xml
repo sync -j4

# 编译完整 Ubuntu/Debian 镜像
./build.sh lunch    # 选择产品后按提示选 ubuntu / debian
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
