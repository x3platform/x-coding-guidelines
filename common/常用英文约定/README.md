开发常用英文约定  

**公共**  

| 英文单词<br />Word      | 描述<br />Description    | 备注<br />Remark  |  
| :--                     | :--                      | :--               | 
| Id | 唯一标识 | nvarchar(36) |  
| Code | 编码 |  |
| Title | 标题 |  |
| Tags | 标签 |  |
| Description | 描述 |  |
| Name | 名称 |  |
| DisplayName | 显示名称 |  |
| GlobalName | 全局名称 |  |
| Content | 内容 |  |
| Reason | 原因 |  |
| PrefixCode | 前缀编号 |  |
| Locking | 锁定 |  |
| OrderId | 排序标识 |  |
| Status | 状态 | 1 启用 0 停用 |
| ModifiedBy | 更新者唯一标识 |  |
| ModifiedDate | 更新时间 |  |
| CreatedBy | 创建者唯一标识 |  |
| CreatedDate | 创建时间 |  |

**人员及权限**

| 英文单词<br />Word      | 描述<br />Description    | 备注<br />Remark  |  
| :--                     | :--                      | :--               | 
| AccountId | 帐号标识 | nvarchar(36) |  
| CorporationId | 公司标识 |  |
| DepartmentId | 部门标识 |  |
| OrganizationId | 组织标识 | 一般指所属末级组织标识 |
| RoleId | 角色标识 |  |
| ProjectId | 项目标识 |  |
| GroupId | 群组标识 |  |
| JobId | 职位标识 |  |
| AssignedJobId | 岗位标识 |  |
| StandardOrganizationId | 标准组织标识 |  |
| StandardRoleId | 标准角色标识 |  |

**工作流**

| 英文单词<br />Word      | 描述<br />Description    | 备注<br />Remark  |  
| :--                     | :--                      | :--               | 
| WorkflowTemplateId | 工作流模板标识 |  |  
| WorkflowInstanceId | 工作流实例标识 |  |
| WorkflowNodeId | 工作流节点标识 |  |
| WorkflowHistoryNodeId | 工作流历史节点标识 |  |
| WorkflowRouteId | 工作流路由标识 |  |
| WorkflowHistoryRouteId | 工作流历史路由标识 |  |
| WorkflowSwitcherId | 工作流分支器标识 |  |
| WorkflowSwitcherExitId | 工作流分支器出口标识 |  |
| WorkflowEntityClassName | 工作流实体类名称 |  |
| WorkflowEntityId | 工作流实体类标识 |  |
| WorkflowActorId | 工作流执行人标识 |  |

**文档信息**

| 英文单词<br />Word      | 描述<br />Description    | 备注<br />Remark  |  
| :--                     | :--                      | :--               | 
| Id | 文档标识 | nvarchar(36) |  
| AccountId | 文档起草人标识 |  |
| AccountName | 文档起草人姓名 |  |
| Code | 文档编号 |  |
| Title | 文档标题 |  |
| CategoryId | 文档类别标识 |  |
| CategoryIndex | 文档类别索引 |  |
| CorporationId | 所属公司标识 |  |
| ProjectId | 所属项目标识 |  |
| Tags | 标签\关键字 |  |
| Content | 内容 |  |
| Links | 相关链接 |  |
| WorkflowEntityId | 工作流实例上的实体类标识 |  |
| DocToken | 文档唯一标识 |  |
| DocVersion | 文档版本 |  |
| DocStatus | 文档状态 |  |
| Status | 状态 |  |
| ModifiedBy | 更新者唯一标识 |  |
| ModifiedDate | 更新时间 |  |
| CreatedBy | 创建者唯一标识 |  |
| CreatedDate | 创建时间 |  |

**文档类别信息**

| 英文单词<br />Word      | 描述<br />Description    | 备注<br />Remark  |  
| :--                     | :--                      | :--               | 
| Id | 文档类别唯一标识 | nvarchar(36) [必填] |  
| AccountId | 文档类别起草人标识 |  |
| AccountName | 文档类别起草人姓名 |  |
| CategoryIndex | 文档类别索引 |  |
| PrefixCode | 文档编号前缀符号 |  |
| Description | 办理说明 |  |
| AuthorizedRoleInstaniated | 角色实例化 1 启用 0 删除 |  |
| WorkflowTemplateId | 工作流模板标识 |  |
| AllowEditWorkflowTemplate | 允许编辑工作流模板 1 启用 0 删除 |  |
| OrderId | 排序标识 |  |
| Status | 状态 1 启用 0 删除 |  |
| Remark | 备注 | nvarchar(200) |
| ModifiedBy | 更新者唯一标识 |  |
| ModifiedDate | 更新时间 |  |
| CreatedBy | 创建者唯一标识 |  |
| CreatedDate | 创建时间 |  |
