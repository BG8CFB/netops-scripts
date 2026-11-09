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

## Pro 包（¥59）— 10 个生产级脚本

| 脚本 | 用途 | 价值 |
|------|------|------|
| batch_config_push.py | 批量下发配置（模板+变量，先 diff 后确认） | 变更窗口神器 |
| port_locator.py | 全网定位 MAC/IP → 接入端口（跨设备 MAC 表追踪） | 排障提速 10x |
| config_audit.py | 基线合规审计（弱口令/telnet/默认VLAN/未用端口） | 等保检查利器 |
| interface_report.py | 接口利用率报表（CRC/带宽/错包）周报自动生成 | 周报自动化 |
| batch_save.py | 批量保存配置 + 时间戳归档 | 配置管理 |
| vlan_map.py | 全网 VLAN 分布地图（哪些交换机有哪些 VLAN） | 网络梳理 |
| stp_root_check.py | STP 根桥位置审计 + 异常检测 | 二层排障 |
| dhcp_snoop_audit.py | DHCP Snooping/ARP 防护配置核查 | 安全合规 |
| syslog_setup.py | 批量配置 syslog 指向采集器 | 日志集中化 |
| batch_reboot.py | 批量重启（维护窗口，二次确认+延时） | 批量操作 |

**购买**: 邮箱 2945362558@qq.com（微信/支付宝 ¥59，发完整包+更新）**

## 设备清单格式（devices.yml）

```yaml
devices:
  - name: core-sw1
    host: 192.168.1.1
    vendor: h3c          # h3c / huawei / cisco / ruijie
    username: admin
    protocol: ssh
```

## 相关项目

- [netcfg-vault](https://github.com/BG8CFB/netcfg-vault) — 批量配置备份 + AES-256-GCM 加密保险库（¥99 Pro）
- [netops-cheatsheets](https://github.com/BG8CFB/netops-cheatsheets) — H3C/华为/思科速查表 + 巡检模板（¥39 Pro）

## License

Free 脚本 MIT。Pro 包内容受版权保护，禁止转售。
