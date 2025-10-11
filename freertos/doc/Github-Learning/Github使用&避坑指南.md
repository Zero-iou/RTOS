#### 如何设置标签？
	在`Settings`中找到`Follow Tags When Sync`配置勾选上
	vscode更多操作里面创建标签
	设置标签名称（建议为功能名称/版本名），设置提交消息
	切换到标签后发布分支
	
![[image-13.png]]
![[image-14.png]]



#### Q&A
#### 1.vscode提交太慢卡着转圈
	解决方法：设置——git——use Editor As commit input的勾选框去掉

#### 2.vscode提交失败
	解决方法：确保网络没问题，必要时候开启VPN代理




#### 注意事项
	千万千万不要在Git Graph里面点击Rebase，否则会一直解决矛盾，回退可以点击Reset
	
![[image-15.png]]

	保持分支同步：定期 git pull 避免冲突，--allow-unrelated-histories参数强制合并
	谨慎使用强制推送，如需清理历史，用 git push --force-with-lease

