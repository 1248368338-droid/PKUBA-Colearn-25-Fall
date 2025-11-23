---
timezone: UTC+8
---

> 请在上边的 timezone 添加你的当地时区(UTC)，这会有助于你的打卡状态的自动化更新，如果没有添加，默认为北京时间 UTC+8 时区


# Donald

1. 自我介绍
我是Donald，对链上数据的分析监控非常感兴趣，希望能够在本次学习中掌握相关知识和技能
2. 你认为你会完成这次共学小组吗？
会的
3. 你感兴趣的小组
链上数据组
4. 你的联系方式（Wechat or Telegram）
TG: @ccaaiw

## Notes

<!-- Content_START -->

### 2025.11.23
1.  **合约间交互范式**
    掌握了链上跨合约调用的标准方法：定义目标合约的 **Interface（接口）**，利用 `InterfaceName(targetAddress).functionName()` 语法进行实例化与调用，实现逻辑的组合与代理执行。

2.  **EVM 日志与 ABI 解码**
    理解了 `indexed` 关键字决定事件参数存储于 **Topics** 还是 **Data**。明确了日志解析完全依赖于 ABI 定义，ABI 与部署代码不一致将导致严重的字节偏移与解码错误。

3.  **调用上下文与权限绕过**
    深刻区分了 `tx.origin`（交易发起者）与 `msg.sender`（当前调用者）。通过部署中间合约（Solver）构建调用链，利用 `msg.sender` 变更的特性，成功绕过 `require(msg.sender != tx.origin)` 限制。

4.  **数据序列化与哈希校验**
    确立了 `keccak256(abi.encodePacked(...))` 为链上数据校验的标准范式。理解了紧凑编码（Packed）的字节级特性，确保链下计算的哈希值与链上逻辑精确匹配。

<!-- Content_END -->
