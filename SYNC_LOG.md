## 同步信息

- **同步时间**: 2026-10-26 12:28:48 UTC
- **上游仓库**: https://github.com/OpenMinis/OpenMinis
- **新增提交**: 3 个

## 更新内容

1a71df0 Merge pull request #495 from OpenMinis/android-1.15-tailscale-fix
b518a7c chore(android): version 1.15 (versionCode 37), the stable release rebuilt with the Tailscale exit-node fix
ee718c6 fix(network,go): traffic through a Tailscale exit node works - host names dial IPv4 first, loopback stays local, an offline exit node refuses instead of leaking direct, and the shell gets IPv4 answers when IPv6 cannot leave

## 文件变更统计

 .github/workflows/build-and-release.yml        |  438 -----
 .github/workflows/sync-upstream.yml            |  120 --
 SYNC_LOG.md                                    | 2207 ------------------------
 deps/rclone-mobile/nethub/dial_tailnet_test.go |  301 ++++
 deps/rclone-mobile/nethub/dns.go               |   38 +
 deps/rclone-mobile/nethub/nethub.go            |  155 +-
 deps/rclone-mobile/nethub/udp.go               |    4 +-
 deps/rclone-mobile/tsnet/proxyview.go          |   14 +-
 deps/rclone-mobile/tsnet/tsnet.go              |   16 +
 src/android/app/build.gradle.kts               |    4 +-
 src/ios/Terminal/.gitkeep                      |    0
 src/shared/network/README.md                   |   15 +-
 src/shared/network/route_vectors.json          |   10 +-
 13 files changed, 542 insertions(+), 2780 deletions(-)
