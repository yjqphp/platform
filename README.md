# platform
分布式服务平台化
## 需求背景
    1、RocketMQ工具化运维：
    
        命令行操作易出错，人力成本高
        
        邮件沟通，沟通效率低、执行速度慢。
        
        历史数据信息不完善
        
    2、平台化运维：
    
        主题管理
        
        组管理
        
        工单管理
        
        消费进度查询
        
## 需求分析  
    
    运维功能选择性支持
    
        创建主题 **
        创建订阅 **
        集群信息查看 *
        创建集群
        集群扩缩容
        
    用户角色划分
    
        普通用户
        管理员
        
    主题信息维护
        
        主题发送方信息
        主题订阅方信息
        主题消费情况
        
    监控与工单提醒
        
        发送超量告警
        消费堆积告警
        工单提醒

## 方案设计
    
    MQ客户端工具
    
    用户权限管理
    
    工单管理
    
    信息展示
    
    DB
    
## 数据库设计

    主题管理表
    
        主题名称
        所属部门
        负责人
        主题描述
        
    工单表
        审批申请
    
    主题申请表
    
        负责人
        归属部门
        主题
        是否延迟消息
        主题描述
        是否申请发送
        
    订阅申请表（以组为单位）
     
        负责人
        归属部门
        主题
        订阅组
        订阅组描述
        堆告警阈值
        
    消费进度
        
        消费落后量
        主题QPS
        
## 功能实现     