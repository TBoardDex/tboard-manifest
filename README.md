# TBoard SDK Download

## Development

```bash
mkdir -p tboard
cd tboard
repo init -u https://github.com/TBoardDex/tboard-manifest.git -b master -m development.xml
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
