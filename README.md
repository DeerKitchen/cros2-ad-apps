# cros2-ad-apps

智驾（AD）应用层聚合仓：多个 ament 包放在 `src/`，消费 `cros2-middleware-vehicle`，不包含 Fast-DDS / vendor 源码。

## Scope

- Domain: **ad** (`base + ad`)
- Runtime: Linux x86_64 / aarch64, ROS 2 Humble, `rmw_fastrtps_cpp`
- Depends: `mw_api`, `company_schema`（经中间件或源码联编）
- Third-party: `cros2-3p-ad` / `cros2-3p-base`（勿把第三方塞进本仓）

## Layout

```text
cros2-ad-apps/
├── src/                 # ament packages (add nodes here)
│   └── ad_apps_meta/    # placeholder meta package
├── launch/              # optional top-level launches
└── docs/
```

## Build (Docker host/vehicle)

```bash
source /opt/ros/humble/setup.bash
# optional: source middleware-vehicle setup
colcon build --base-paths src
```

## Manifest

Register in `cros2-manifest/profiles/deps/ad.repos` and lock.  
Guide: `cros2-docs-governance/docs/16_THREE_DOMAIN_APPLICATION_REPO_GUIDE.md`
