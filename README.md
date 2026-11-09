# netops-scripts — 网络工程师自动化脚本包

> Network engineer automation script pack — H3C / Huawei / Cisco / Ruijie
> 网络运维自动化脚本 / network automation scripts / 批量巡检脚本 / 批量配置脚本

## 免费脚本（Free）

| 脚本 | 用途 |
|------|------|
| [`batch_info.py`](scripts/batch_info.py) | 批量采集设备信息（版本/CPU/内存/接口状态），输出 CSV |
| [`find_ip.py`](scripts/find_ip.py) | 在所有设备配置中搜索某个 IP/MAC 出现位置（定位接入端口） |

```bash
pip install paramiko
python batch_info.py devices.yml
```



## Pro 脚本包（¥59，6 个独占脚本）

免费版（2 个）已进 PyPI 包 [netops-toolkit](https://pypi.org/project/netops-toolkit/)（info/find/save/interfaces/locate/audit 六子命令）。
Pro 是 **netops-toolkit 没有的 6 个高危操作脚本**——改动型/批量型，企业内部场景刚需：

| # | 脚本 | 能力 | 为什么值得 |
|---|---|---|---|
| 1 | batch_config_push.py | 模板+变量批量下发配置 | 变更窗口一次改 200 台，预览+确认+并发 |
| 2 | batch_reboot.py | 批量重启（二次确认+延时） | 深夜割接必备，避免逐台敲 |
| 3 | syslog_setup.py | 四厂商 syslog+save 一键配置 | 等保/审计合规第一步 |
| 4 | vlan_map.py | 全网 VLAN 分布表+孤儿 VLAN 检出 | 清理僵尸 VLAN，防环路隐患 |
| 5 | stp_root_check.py | 根桥校验+漂移告警 | 根桥漂移=环路前兆，--expect-root 校验 |
| 6 | dhcp_snoop_audit.py | DHCP Snooping 三项合规检查 | 防私接路由器的标配 |

**交付方式**: 邮件发送全部 6 个 .py（无加密、无 license 文件，一次买断）+ 后续更新免费。
**购买**: 邮箱 2945362558@qq.com（注明 netops-scripts Pro）
