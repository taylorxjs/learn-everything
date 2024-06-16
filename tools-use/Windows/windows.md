# 网络

**更改你的DNS服务器** 如果刷新DNS缓存解决不了问题，你应该尝试更改你的DNS服务器。你可以更改为Google的公共DNS服务器，以下是如何更改：

在*Windows*上：

1. 打开网络设置（`Settings > Network & Internet > Change adapter options`）。
2. 然后在你的网络连接上点击右键，选择“Properties（属性）”。
3. 双击“Internet Protocol Version 4 (TCP/IPv4)/Internet Protocol Version 6 (TCP/IPv6)”。
4. 选择“Use the following DNS server addresses”，然后输入下面的地址：
   - 对于IPv4：8.8.8.8 和 8.8.4.4
   - 对于IPv6：2001:4860:4860::8888 和 2001:4860:4860::8844

# 文件

在Windows 10系统中关闭文件预览功能，可以按照以下步骤操作：

1. 打开任意一个文件夹。
2. 在文件夹的顶部菜单栏中，点击“查看”选项。
3. 在“查看”菜单下，找到并取消勾选“预览窗格”选项。这通常位于“显示/隐藏”部分。

通过以上步骤，文件预览功能就会被关闭，之后在文件资源管理器中浏览文件时，右侧的预览窗格将不再显示文件内容预览。

如果你希望通过注册表编辑器来彻底关闭此功能，可以按照以下高级步骤操作（需谨慎操作注册表）：

1. 按Win+R键打开“运行”对话框，输入`regedit`后按回车，打开注册表编辑器。
2. 定位到以下路径：
   ```
   HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced
   ```
3. 在右侧窗格中，找到名为`DisabledPreviewPane`的DWORD值。如果不存在，你需要右键点击右侧空白区域，选择“新建” -> “DWORD (32位) 值”，然后命名为`DisabledPreviewPane`。
4. 双击`DisabledPreviewPane`，在弹出的对话框中，将数值数据改为`1`，然后点击“确定”。
5. 重启文件资源管理器或注销并重新登录系统以使更改生效。

请注意，修改注册表前最好备份相关键值或整个注册表，以防操作失误导致问题。