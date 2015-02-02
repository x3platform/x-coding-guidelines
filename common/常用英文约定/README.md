开发常用英文约定  

**公共**  

| 英文单词<br />Word      | 描述<br />Description    | 备注<br />Remark  |  
| :--                     | :--                      | :--               | 
| Id | 唯一标识 | nvarchar(36) |  
| Code | 编码 |  |
| ModifiedBy | 更新者唯一标识 |  |
| ModifiedDate | 更新时间 |  |
| CreatedBy | 创建者唯一标识 |  |
| CreatedDate | 创建时间 |  |

**人员及权限**

**工作流**

**文档信息**

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
