# Docker 镜像盘点（fork: chenmins/rio）

本仓库当前直接涉及的 `rancher/rio*` 系列镜像共 **3 个**，建议统一迁移到 `chenmins/*`：

1. `rancher/rio-controller` → `chenmins/rio-controller`
2. `rancher/rio-autoscaler` → `chenmins/rio-autoscaler`
3. `rancher/rio-dashboard` → `chenmins/rio-dashboard`

> 说明：本仓库可直接构建的镜像是 `rio-controller`（`package/Dockerfile`），其他镜像（autoscaler/dashboard）需要在各自源码仓库或独立 Dockerfile 中构建。

## 发布建议

- 本仓库通过 GitHub Actions 在 tag 发布时自动构建并推送 `chenmins/rio-controller` 多架构镜像。
- `rio-autoscaler`、`rio-dashboard` 建议在其各自仓库建立同样的发布流水线，并在本仓库只保留引用。
