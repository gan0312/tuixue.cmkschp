# 蛇口母港船票 自动爬取+推送通知

主要用于爬取蛇口母港-香港国际机场的船票，支持批量爬取以及Bark推送提醒。

# 安装

程序在Python 3.8与3.9测试通过。

安装依赖库：

```shell
pip install -r requirements.txt
```

# 使用

本程序的主要配置在`main.py`中设置。

```python
# ==================================
# Global Settings
# Bark Push
enable_bark = False         # 启用Bark推送
bark_token = ""             # Bark推送ID
# Ticket Stuff
startSite = "SK"            # 始发站点
endSite = "HKA"             # 目标站点
startDate = "2021-08-1"     # 船票搜索日期
endDate = "2021-08-18"
show_available_only = True  # 只显示有票的日期
# ==================================
```

配置完成后运行`python3 main.py`自动抓取相应日期的船票。

# Bark推送(iOS Only)

安装好bark app，复制测试URL中的key至`main.py`中的`bark_token = ""`并且将`enable_bark = False`改为`True`

# 未来计划（不一定填坑）

- 前端网页
- 邮件推送

# Credits

感谢[tuixue.online](https://github.com/Trinkle23897/tuixue.online-visa) 的灵感。

**愿天下所有人都不用退学**