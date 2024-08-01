# 技术栈
React + Arco Design + SpringBoot + Mybaits Plus+ Docker + Knife4j
# 项目描述
本项目是为编程学习人员提供的在线题目评测系统(Online Judge)。系统可以依据预设测试样例，执行用户提交的代码并判断是否符合题目要求。
# features
- 自主实现代码沙箱，且服务独立，提供两种接入方式供开发者使用
    1. **SpringBoot Starter**, 导入Jar包, 直接注入代码沙箱Bean，调用代码执行方法即可使用
    2. **Restful API**, 通过发送Http请求，使用代码执行接口
- 代码沙箱使用Docker容器执行代码。与主机环境隔离，提高了安全性且便于监控。抽象出一套统一的`编译+执行代码`的逻辑，编写实现此逻辑的shell脚本即可拓展一个语言的执行器，无需修改源代码
- 使用 apache common pool2 池化技术管理 Docker 会话，实现会话复用，减小频繁的创建销毁会话带来的性能那开销；控制会话数，简化资源管理，防止过多的会话积压导致服务崩溃
# 架构图
