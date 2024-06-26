**Example 1: 更新角色（带权限树参数）**

更新角色并同时设置角色中的权限内容，设置权限树参数 PermissionGroups ，PermissionGroups 展开为树形结构，可以需要的权限节点下将 IsChecked 属性设置为true。
注意：父权限节点 IsChecked 属性为true，则需要将其下所有子节点的 IsChecked属性同时设置为true，否则校验不通过。

Input: 

```
tccli essbasic ChannelModifyRole --cli-unfold-argument  \
    --Agent.AppId  jsdk812kxkdfjks***k88123123 \
    --Agent.ProxyOrganizationOpenId test_org_openid \
    --Agent.ProxyOperator.OpenId test_openid \
    --RoleId 123456**89 \
    --Name xxx角色 \
    --Description 这是一个自定义角色 \
    --PermissionGroups.0.GroupKey bill \
    --PermissionGroups.0.GroupName 费用中心 \
    --PermissionGroups.0.Hide 0 \
    --PermissionGroups.0.Permissions.0.Children.0.DataLabel 0 \
    --PermissionGroups.0.Permissions.0.Children.0.DataRange 0 \
    --PermissionGroups.0.Permissions.0.Children.0.DataTo  \
    --PermissionGroups.0.Permissions.0.Children.0.DataType 0 \
    --PermissionGroups.0.Permissions.0.Children.0.Hide 1 \
    --PermissionGroups.0.Permissions.0.Children.0.IsChecked False \
    --PermissionGroups.0.Permissions.0.Children.0.Key BillOrderManagement \
    --PermissionGroups.0.Permissions.0.Children.0.Name 订单管理 \
    --PermissionGroups.0.Permissions.0.Children.0.ParentKey  \
    --PermissionGroups.0.Permissions.0.Children.0.Type 2 \
    --PermissionGroups.0.Permissions.0.Children.1.DataLabel 0 \
    --PermissionGroups.0.Permissions.0.Children.1.DataRange 0 \
    --PermissionGroups.0.Permissions.0.Children.1.DataTo  \
    --PermissionGroups.0.Permissions.0.Children.1.DataType 0 \
    --PermissionGroups.0.Permissions.0.Children.1.Hide 1 \
    --PermissionGroups.0.Permissions.0.Children.1.IsChecked False \
    --PermissionGroups.0.Permissions.0.Children.1.Key BillSetMealManagement \
    --PermissionGroups.0.Permissions.0.Children.1.Name 套餐管理 \
    --PermissionGroups.0.Permissions.0.Children.1.ParentKey  \
    --PermissionGroups.0.Permissions.0.Children.1.Type 2 \
    --PermissionGroups.0.Permissions.0.Children.2.DataLabel 0 \
    --PermissionGroups.0.Permissions.0.Children.2.DataRange 0 \
    --PermissionGroups.0.Permissions.0.Children.2.DataTo  \
    --PermissionGroups.0.Permissions.0.Children.2.DataType 0 \
    --PermissionGroups.0.Permissions.0.Children.2.Hide 1 \
    --PermissionGroups.0.Permissions.0.Children.2.IsChecked False \
    --PermissionGroups.0.Permissions.0.Children.2.Key BillInvoiceManagement \
    --PermissionGroups.0.Permissions.0.Children.2.Name 发票管理 \
    --PermissionGroups.0.Permissions.0.Children.2.ParentKey  \
    --PermissionGroups.0.Permissions.0.Children.2.Type 2 \
    --PermissionGroups.0.Permissions.0.DataLabel 0 \
    --PermissionGroups.0.Permissions.0.DataRange 0 \
    --PermissionGroups.0.Permissions.0.DataTo  \
    --PermissionGroups.0.Permissions.0.DataType 0 \
    --PermissionGroups.0.Permissions.0.Hide 0 \
    --PermissionGroups.0.Permissions.0.IsChecked False \
    --PermissionGroups.0.Permissions.0.Key BillManagement \
    --PermissionGroups.0.Permissions.0.Name 费用管理 \
    --PermissionGroups.0.Permissions.0.ParentKey  \
    --PermissionGroups.0.Permissions.0.Type 1 \
    --PermissionGroups.1.GroupKey channel \
    --PermissionGroups.1.GroupName 开发者中心 \
    --PermissionGroups.1.Hide 0 \
    --PermissionGroups.1.Permissions.0.Children.0.DataLabel 0 \
    --PermissionGroups.1.Permissions.0.Children.0.DataRange 0 \
    --PermissionGroups.1.Permissions.0.Children.0.DataTo  \
    --PermissionGroups.1.Permissions.0.Children.0.DataType 0 \
    --PermissionGroups.1.Permissions.0.Children.0.Hide 1 \
    --PermissionGroups.1.Permissions.0.Children.0.IsChecked False \
    --PermissionGroups.1.Permissions.0.Children.0.Key DescribeChannelComponents \
    --PermissionGroups.1.Permissions.0.Children.0.Name 渠道控件查看 \
    --PermissionGroups.1.Permissions.0.Children.0.ParentKey  \
    --PermissionGroups.1.Permissions.0.Children.0.Type 2 \
    --PermissionGroups.1.Permissions.0.Children.1.DataLabel 0 \
    --PermissionGroups.1.Permissions.0.Children.1.DataRange 0 \
    --PermissionGroups.1.Permissions.0.Children.1.DataTo  \
    --PermissionGroups.1.Permissions.0.Children.1.DataType 0 \
    --PermissionGroups.1.Permissions.0.Children.1.Hide 1 \
    --PermissionGroups.1.Permissions.0.Children.1.IsChecked False \
    --PermissionGroups.1.Permissions.0.Children.1.Key InsertOrModifyChannelComponents \
    --PermissionGroups.1.Permissions.0.Children.1.Name 渠道控件编辑 \
    --PermissionGroups.1.Permissions.0.Children.1.ParentKey  \
    --PermissionGroups.1.Permissions.0.Children.1.Type 2 \
    --PermissionGroups.1.Permissions.0.Children.2.DataLabel 0 \
    --PermissionGroups.1.Permissions.0.Children.2.DataRange 0 \
    --PermissionGroups.1.Permissions.0.Children.2.DataTo  \
    --PermissionGroups.1.Permissions.0.Children.2.DataType 0 \
    --PermissionGroups.1.Permissions.0.Children.2.Hide 1 \
    --PermissionGroups.1.Permissions.0.Children.2.IsChecked False \
    --PermissionGroups.1.Permissions.0.Children.2.Key DeleteChannelComponents \
    --PermissionGroups.1.Permissions.0.Children.2.Name 渠道控件删除 \
    --PermissionGroups.1.Permissions.0.Children.2.ParentKey  \
    --PermissionGroups.1.Permissions.0.Children.2.Type 2 \
    --PermissionGroups.1.Permissions.0.DataLabel 0 \
    --PermissionGroups.1.Permissions.0.DataRange 0 \
    --PermissionGroups.1.Permissions.0.DataTo  \
    --PermissionGroups.1.Permissions.0.DataType 0 \
    --PermissionGroups.1.Permissions.0.Hide 0 \
    --PermissionGroups.1.Permissions.0.IsChecked False \
    --PermissionGroups.1.Permissions.0.Key WidgetManagement \
    --PermissionGroups.1.Permissions.0.Name 渠道模板控件管理 \
    --PermissionGroups.1.Permissions.0.ParentKey  \
    --PermissionGroups.1.Permissions.0.Type 1 \
    --PermissionGroups.1.Permissions.1.Children.0.DataLabel 0 \
    --PermissionGroups.1.Permissions.1.Children.0.DataRange 0 \
    --PermissionGroups.1.Permissions.1.Children.0.DataTo  \
    --PermissionGroups.1.Permissions.1.Children.0.DataType 0 \
    --PermissionGroups.1.Permissions.1.Children.0.Hide 1 \
    --PermissionGroups.1.Permissions.1.Children.0.IsChecked False \
    --PermissionGroups.1.Permissions.1.Children.0.Key DescribeChannelTemplate \
    --PermissionGroups.1.Permissions.1.Children.0.Name 渠道模板库查看 \
    --PermissionGroups.1.Permissions.1.Children.0.ParentKey  \
    --PermissionGroups.1.Permissions.1.Children.0.Type 2 \
    --PermissionGroups.1.Permissions.1.Children.1.DataLabel 0 \
    --PermissionGroups.1.Permissions.1.Children.1.DataRange 0 \
    --PermissionGroups.1.Permissions.1.Children.1.DataTo  \
    --PermissionGroups.1.Permissions.1.Children.1.DataType 0 \
    --PermissionGroups.1.Permissions.1.Children.1.Hide 1 \
    --PermissionGroups.1.Permissions.1.Children.1.IsChecked False \
    --PermissionGroups.1.Permissions.1.Children.1.Key InsertOrModifyChannelTemplate \
    --PermissionGroups.1.Permissions.1.Children.1.Name 渠道模板库编辑 \
    --PermissionGroups.1.Permissions.1.Children.1.ParentKey  \
    --PermissionGroups.1.Permissions.1.Children.1.Type 2 \
    --PermissionGroups.1.Permissions.1.Children.2.DataLabel 0 \
    --PermissionGroups.1.Permissions.1.Children.2.DataRange 0 \
    --PermissionGroups.1.Permissions.1.Children.2.DataTo  \
    --PermissionGroups.1.Permissions.1.Children.2.DataType 0 \
    --PermissionGroups.1.Permissions.1.Children.2.Hide 1 \
    --PermissionGroups.1.Permissions.1.Children.2.IsChecked False \
    --PermissionGroups.1.Permissions.1.Children.2.Key DeleteChannelTemplate \
    --PermissionGroups.1.Permissions.1.Children.2.Name 渠道模板库删除 \
    --PermissionGroups.1.Permissions.1.Children.2.ParentKey  \
    --PermissionGroups.1.Permissions.1.Children.2.Type 2 \
    --PermissionGroups.1.Permissions.1.DataLabel 0 \
    --PermissionGroups.1.Permissions.1.DataRange 0 \
    --PermissionGroups.1.Permissions.1.DataTo  \
    --PermissionGroups.1.Permissions.1.DataType 0 \
    --PermissionGroups.1.Permissions.1.Hide 0 \
    --PermissionGroups.1.Permissions.1.IsChecked False \
    --PermissionGroups.1.Permissions.1.Key ChannelTemplateManagement \
    --PermissionGroups.1.Permissions.1.Name 渠道模板库管理 \
    --PermissionGroups.1.Permissions.1.ParentKey  \
    --PermissionGroups.1.Permissions.1.Type 1 \
    --PermissionGroups.2.GroupKey Flow \
    --PermissionGroups.2.GroupName 合同中心 \
    --PermissionGroups.2.Hide 0 \
    --PermissionGroups.2.Permissions.0.Children.0.DataLabel 2 \
    --PermissionGroups.2.Permissions.0.Children.0.DataRange 1 \
    --PermissionGroups.2.Permissions.0.Children.0.DataTo  \
    --PermissionGroups.2.Permissions.0.Children.0.DataType 0 \
    --PermissionGroups.2.Permissions.0.Children.0.Hide 0 \
    --PermissionGroups.2.Permissions.0.Children.0.IsChecked False \
    --PermissionGroups.2.Permissions.0.Children.0.Key DescribeAllFlows \
    --PermissionGroups.2.Permissions.0.Children.0.Name 企业全部合同 \
    --PermissionGroups.2.Permissions.0.Children.0.ParentKey FlowsManagement \
    --PermissionGroups.2.Permissions.0.Children.0.Type 2 \
    --PermissionGroups.2.Permissions.0.DataLabel 1 \
    --PermissionGroups.2.Permissions.0.DataRange 0 \
    --PermissionGroups.2.Permissions.0.DataTo  \
    --PermissionGroups.2.Permissions.0.DataType 2 \
    --PermissionGroups.2.Permissions.0.Hide 0 \
    --PermissionGroups.2.Permissions.0.IsChecked False \
    --PermissionGroups.2.Permissions.0.Key FlowsManagement \
    --PermissionGroups.2.Permissions.0.Name 查询合同 \
    --PermissionGroups.2.Permissions.0.ParentKey  \
    --PermissionGroups.2.Permissions.0.Type 1 \
    --PermissionGroups.2.Permissions.1.DataLabel 1 \
    --PermissionGroups.2.Permissions.1.DataRange 0 \
    --PermissionGroups.2.Permissions.1.DataTo FlowsManagement \
    --PermissionGroups.2.Permissions.1.DataType 1 \
    --PermissionGroups.2.Permissions.1.Hide 0 \
    --PermissionGroups.2.Permissions.1.IsChecked False \
    --PermissionGroups.2.Permissions.1.Key FlowsManagement-Preview \
    --PermissionGroups.2.Permissions.1.Name 合同详情&预览 \
    --PermissionGroups.2.Permissions.1.ParentKey  \
    --PermissionGroups.2.Permissions.1.Type 1 \
    --PermissionGroups.2.Permissions.2.DataLabel 1 \
    --PermissionGroups.2.Permissions.2.DataRange 0 \
    --PermissionGroups.2.Permissions.2.DataTo FlowsManagement \
    --PermissionGroups.2.Permissions.2.DataType 1 \
    --PermissionGroups.2.Permissions.2.Hide 0 \
    --PermissionGroups.2.Permissions.2.IsChecked False \
    --PermissionGroups.2.Permissions.2.Key FlowsManagement-Download \
    --PermissionGroups.2.Permissions.2.Name 下载合同 \
    --PermissionGroups.2.Permissions.2.ParentKey  \
    --PermissionGroups.2.Permissions.2.Type 1 \
    --PermissionGroups.2.Permissions.3.Children.0.DataLabel 0 \
    --PermissionGroups.2.Permissions.3.Children.0.DataRange 0 \
    --PermissionGroups.2.Permissions.3.Children.0.DataTo  \
    --PermissionGroups.2.Permissions.3.Children.0.DataType 0 \
    --PermissionGroups.2.Permissions.3.Children.0.Hide 0 \
    --PermissionGroups.2.Permissions.3.Children.0.IsChecked False \
    --PermissionGroups.2.Permissions.3.Children.0.Key FlowByImportedFile \
    --PermissionGroups.2.Permissions.3.Children.0.Name 上传文件发起 \
    --PermissionGroups.2.Permissions.3.Children.0.ParentKey  \
    --PermissionGroups.2.Permissions.3.Children.0.Type 2 \
    --PermissionGroups.2.Permissions.3.Children.1.DataLabel 0 \
    --PermissionGroups.2.Permissions.3.Children.1.DataRange 0 \
    --PermissionGroups.2.Permissions.3.Children.1.DataTo  \
    --PermissionGroups.2.Permissions.3.Children.1.DataType 0 \
    --PermissionGroups.2.Permissions.3.Children.1.Hide 0 \
    --PermissionGroups.2.Permissions.3.Children.1.IsChecked False \
    --PermissionGroups.2.Permissions.3.Children.1.Key FlowByOrganizationTemplate \
    --PermissionGroups.2.Permissions.3.Children.1.Name 企业模版发起 \
    --PermissionGroups.2.Permissions.3.Children.1.ParentKey  \
    --PermissionGroups.2.Permissions.3.Children.1.Type 1 \
    --PermissionGroups.2.Permissions.3.Children.2.DataLabel 0 \
    --PermissionGroups.2.Permissions.3.Children.2.DataRange 0 \
    --PermissionGroups.2.Permissions.3.Children.2.DataTo  \
    --PermissionGroups.2.Permissions.3.Children.2.DataType 0 \
    --PermissionGroups.2.Permissions.3.Children.2.Hide 0 \
    --PermissionGroups.2.Permissions.3.Children.2.IsChecked False \
    --PermissionGroups.2.Permissions.3.Children.2.Key CreateMultiFlowSignQRCode \
    --PermissionGroups.2.Permissions.3.Children.2.Name 创建签署二维码 \
    --PermissionGroups.2.Permissions.3.Children.2.ParentKey  \
    --PermissionGroups.2.Permissions.3.Children.2.Type 1 \
    --PermissionGroups.2.Permissions.3.DataLabel 0 \
    --PermissionGroups.2.Permissions.3.DataRange 0 \
    --PermissionGroups.2.Permissions.3.DataTo  \
    --PermissionGroups.2.Permissions.3.DataType 0 \
    --PermissionGroups.2.Permissions.3.Hide 0 \
    --PermissionGroups.2.Permissions.3.IsChecked False \
    --PermissionGroups.2.Permissions.3.Key CreateFlow \
    --PermissionGroups.2.Permissions.3.Name 发起合同 \
    --PermissionGroups.2.Permissions.3.ParentKey  \
    --PermissionGroups.2.Permissions.3.Type 2 \
    --PermissionGroups.2.Permissions.4.DataLabel 0 \
    --PermissionGroups.2.Permissions.4.DataRange 0 \
    --PermissionGroups.2.Permissions.4.DataTo  \
    --PermissionGroups.2.Permissions.4.DataType 0 \
    --PermissionGroups.2.Permissions.4.Hide 1 \
    --PermissionGroups.2.Permissions.4.IsChecked False \
    --PermissionGroups.2.Permissions.4.Key FlowsManagement-Pickup \
    --PermissionGroups.2.Permissions.4.Name 领取合同 \
    --PermissionGroups.2.Permissions.4.ParentKey  \
    --PermissionGroups.2.Permissions.4.Type 1 \
    --PermissionGroups.2.Permissions.5.DataLabel 0 \
    --PermissionGroups.2.Permissions.5.DataRange 0 \
    --PermissionGroups.2.Permissions.5.DataTo  \
    --PermissionGroups.2.Permissions.5.DataType 0 \
    --PermissionGroups.2.Permissions.5.Hide 0 \
    --PermissionGroups.2.Permissions.5.IsChecked False \
    --PermissionGroups.2.Permissions.5.Key CancelFlow \
    --PermissionGroups.2.Permissions.5.Name 撤销合同 \
    --PermissionGroups.2.Permissions.5.ParentKey  \
    --PermissionGroups.2.Permissions.5.Type 2 \
    --PermissionGroups.3.GroupKey Organization \
    --PermissionGroups.3.GroupName 组织员工 \
    --PermissionGroups.3.Hide 0 \
    --PermissionGroups.3.Permissions.0.Children.0.DataLabel 0 \
    --PermissionGroups.3.Permissions.0.Children.0.DataRange 0 \
    --PermissionGroups.3.Permissions.0.Children.0.DataTo  \
    --PermissionGroups.3.Permissions.0.Children.0.DataType 0 \
    --PermissionGroups.3.Permissions.0.Children.0.Hide 1 \
    --PermissionGroups.3.Permissions.0.Children.0.IsChecked False \
    --PermissionGroups.3.Permissions.0.Children.0.Key CreateUserRoles \
    --PermissionGroups.3.Permissions.0.Children.0.Name 为员工分配角色 \
    --PermissionGroups.3.Permissions.0.Children.0.ParentKey  \
    --PermissionGroups.3.Permissions.0.Children.0.Type 2 \
    --PermissionGroups.3.Permissions.0.Children.1.DataLabel 0 \
    --PermissionGroups.3.Permissions.0.Children.1.DataRange 0 \
    --PermissionGroups.3.Permissions.0.Children.1.DataTo  \
    --PermissionGroups.3.Permissions.0.Children.1.DataType 0 \
    --PermissionGroups.3.Permissions.0.Children.1.Hide 1 \
    --PermissionGroups.3.Permissions.0.Children.1.IsChecked False \
    --PermissionGroups.3.Permissions.0.Children.1.Key ModifyYuFuOrg \
    --PermissionGroups.3.Permissions.0.Children.1.Name 编辑组织架构 \
    --PermissionGroups.3.Permissions.0.Children.1.ParentKey  \
    --PermissionGroups.3.Permissions.0.Children.1.Type 1 \
    --PermissionGroups.3.Permissions.0.DataLabel 0 \
    --PermissionGroups.3.Permissions.0.DataRange 0 \
    --PermissionGroups.3.Permissions.0.DataTo  \
    --PermissionGroups.3.Permissions.0.DataType 0 \
    --PermissionGroups.3.Permissions.0.Hide 0 \
    --PermissionGroups.3.Permissions.0.IsChecked False \
    --PermissionGroups.3.Permissions.0.Key OrgManagement \
    --PermissionGroups.3.Permissions.0.Name 组织架构管理 \
    --PermissionGroups.3.Permissions.0.ParentKey  \
    --PermissionGroups.3.Permissions.0.Type 1 \
    --PermissionGroups.3.Permissions.1.Children.0.DataLabel 0 \
    --PermissionGroups.3.Permissions.1.Children.0.DataRange 0 \
    --PermissionGroups.3.Permissions.1.Children.0.DataTo  \
    --PermissionGroups.3.Permissions.1.Children.0.DataType 0 \
    --PermissionGroups.3.Permissions.1.Children.0.Hide 1 \
    --PermissionGroups.3.Permissions.1.Children.0.IsChecked False \
    --PermissionGroups.3.Permissions.1.Children.0.Key CreateRole \
    --PermissionGroups.3.Permissions.1.Children.0.Name 创建角色 \
    --PermissionGroups.3.Permissions.1.Children.0.ParentKey  \
    --PermissionGroups.3.Permissions.1.Children.0.Type 2 \
    --PermissionGroups.3.Permissions.1.Children.1.DataLabel 0 \
    --PermissionGroups.3.Permissions.1.Children.1.DataRange 0 \
    --PermissionGroups.3.Permissions.1.Children.1.DataTo  \
    --PermissionGroups.3.Permissions.1.Children.1.DataType 0 \
    --PermissionGroups.3.Permissions.1.Children.1.Hide 1 \
    --PermissionGroups.3.Permissions.1.Children.1.IsChecked False \
    --PermissionGroups.3.Permissions.1.Children.1.Key ModifyRole \
    --PermissionGroups.3.Permissions.1.Children.1.Name 修改角色 \
    --PermissionGroups.3.Permissions.1.Children.1.ParentKey  \
    --PermissionGroups.3.Permissions.1.Children.1.Type 2 \
    --PermissionGroups.3.Permissions.1.Children.2.DataLabel 0 \
    --PermissionGroups.3.Permissions.1.Children.2.DataRange 0 \
    --PermissionGroups.3.Permissions.1.Children.2.DataTo  \
    --PermissionGroups.3.Permissions.1.Children.2.DataType 0 \
    --PermissionGroups.3.Permissions.1.Children.2.Hide 1 \
    --PermissionGroups.3.Permissions.1.Children.2.IsChecked False \
    --PermissionGroups.3.Permissions.1.Children.2.Key DeleteRole \
    --PermissionGroups.3.Permissions.1.Children.2.Name 删除角色 \
    --PermissionGroups.3.Permissions.1.Children.2.ParentKey  \
    --PermissionGroups.3.Permissions.1.Children.2.Type 2 \
    --PermissionGroups.3.Permissions.1.Children.3.DataLabel 0 \
    --PermissionGroups.3.Permissions.1.Children.3.DataRange 0 \
    --PermissionGroups.3.Permissions.1.Children.3.DataTo  \
    --PermissionGroups.3.Permissions.1.Children.3.DataType 0 \
    --PermissionGroups.3.Permissions.1.Children.3.Hide 1 \
    --PermissionGroups.3.Permissions.1.Children.3.IsChecked False \
    --PermissionGroups.3.Permissions.1.Children.3.Key ModifyRoleStatus \
    --PermissionGroups.3.Permissions.1.Children.3.Name 启用&禁用角色 \
    --PermissionGroups.3.Permissions.1.Children.3.ParentKey  \
    --PermissionGroups.3.Permissions.1.Children.3.Type 2 \
    --PermissionGroups.3.Permissions.1.Children.4.DataLabel 0 \
    --PermissionGroups.3.Permissions.1.Children.4.DataRange 0 \
    --PermissionGroups.3.Permissions.1.Children.4.DataTo  \
    --PermissionGroups.3.Permissions.1.Children.4.DataType 0 \
    --PermissionGroups.3.Permissions.1.Children.4.Hide 1 \
    --PermissionGroups.3.Permissions.1.Children.4.IsChecked False \
    --PermissionGroups.3.Permissions.1.Children.4.Key CreateRoleUsers \
    --PermissionGroups.3.Permissions.1.Children.4.Name 添加员工 \
    --PermissionGroups.3.Permissions.1.Children.4.ParentKey  \
    --PermissionGroups.3.Permissions.1.Children.4.Type 2 \
    --PermissionGroups.3.Permissions.1.Children.5.DataLabel 0 \
    --PermissionGroups.3.Permissions.1.Children.5.DataRange 0 \
    --PermissionGroups.3.Permissions.1.Children.5.DataTo  \
    --PermissionGroups.3.Permissions.1.Children.5.DataType 0 \
    --PermissionGroups.3.Permissions.1.Children.5.Hide 1 \
    --PermissionGroups.3.Permissions.1.Children.5.IsChecked False \
    --PermissionGroups.3.Permissions.1.Children.5.Key DeleteRoleUsers \
    --PermissionGroups.3.Permissions.1.Children.5.Name 取消关联 \
    --PermissionGroups.3.Permissions.1.Children.5.ParentKey  \
    --PermissionGroups.3.Permissions.1.Children.5.Type 2 \
    --PermissionGroups.3.Permissions.1.DataLabel 0 \
    --PermissionGroups.3.Permissions.1.DataRange 0 \
    --PermissionGroups.3.Permissions.1.DataTo  \
    --PermissionGroups.3.Permissions.1.DataType 0 \
    --PermissionGroups.3.Permissions.1.Hide 0 \
    --PermissionGroups.3.Permissions.1.IsChecked False \
    --PermissionGroups.3.Permissions.1.Key RoleManagement \
    --PermissionGroups.3.Permissions.1.Name 角色管理 \
    --PermissionGroups.3.Permissions.1.ParentKey  \
    --PermissionGroups.3.Permissions.1.Type 1 \
    --PermissionGroups.4.GroupKey Seal \
    --PermissionGroups.4.GroupName 印章中心 \
    --PermissionGroups.4.Hide 0 \
    --PermissionGroups.4.Permissions.0.Children.0.DataLabel 0 \
    --PermissionGroups.4.Permissions.0.Children.0.DataRange 0 \
    --PermissionGroups.4.Permissions.0.Children.0.DataTo  \
    --PermissionGroups.4.Permissions.0.Children.0.DataType 0 \
    --PermissionGroups.4.Permissions.0.Children.0.Hide 1 \
    --PermissionGroups.4.Permissions.0.Children.0.IsChecked False \
    --PermissionGroups.4.Permissions.0.Children.0.Key QueryHoldSeal \
    --PermissionGroups.4.Permissions.0.Children.0.Name 查询印章 \
    --PermissionGroups.4.Permissions.0.Children.0.ParentKey  \
    --PermissionGroups.4.Permissions.0.Children.0.Type 2 \
    --PermissionGroups.4.Permissions.0.DataLabel 0 \
    --PermissionGroups.4.Permissions.0.DataRange 0 \
    --PermissionGroups.4.Permissions.0.DataTo  \
    --PermissionGroups.4.Permissions.0.DataType 0 \
    --PermissionGroups.4.Permissions.0.Hide 0 \
    --PermissionGroups.4.Permissions.0.IsChecked False \
    --PermissionGroups.4.Permissions.0.Key SealManagement-Hold \
    --PermissionGroups.4.Permissions.0.Name 我持有企业印章 \
    --PermissionGroups.4.Permissions.0.ParentKey  \
    --PermissionGroups.4.Permissions.0.Type 1 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.0.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.0.DataRange 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.0.DataTo  \
    --PermissionGroups.4.Permissions.1.Children.0.Children.0.DataType 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.0.Hide 1 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.0.IsChecked False \
    --PermissionGroups.4.Permissions.1.Children.0.Children.0.Key SealManagement-Manage-Detail-Holder \
    --PermissionGroups.4.Permissions.1.Children.0.Children.0.Name 授权记录 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.0.ParentKey  \
    --PermissionGroups.4.Permissions.1.Children.0.Children.0.Type 2 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.1.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.1.DataRange 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.1.DataTo  \
    --PermissionGroups.4.Permissions.1.Children.0.Children.1.DataType 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.1.Hide 1 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.1.IsChecked False \
    --PermissionGroups.4.Permissions.1.Children.0.Children.1.Key SealManagement-Manage-Detail-Holder-Template \
    --PermissionGroups.4.Permissions.1.Children.0.Children.1.Name 关联模版 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.1.ParentKey  \
    --PermissionGroups.4.Permissions.1.Children.0.Children.1.Type 2 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.2.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.2.DataRange 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.2.DataTo  \
    --PermissionGroups.4.Permissions.1.Children.0.Children.2.DataType 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.2.Hide 1 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.2.IsChecked False \
    --PermissionGroups.4.Permissions.1.Children.0.Children.2.Key SealManagement-Manage-Detail-Holder-Use-Record \
    --PermissionGroups.4.Permissions.1.Children.0.Children.2.Name 用印记录 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.2.ParentKey  \
    --PermissionGroups.4.Permissions.1.Children.0.Children.2.Type 2 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.3.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.3.DataRange 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.3.DataTo  \
    --PermissionGroups.4.Permissions.1.Children.0.Children.3.DataType 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.3.Hide 1 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.3.IsChecked False \
    --PermissionGroups.4.Permissions.1.Children.0.Children.3.Key SealManagement-Manage-Detail-Holder-Change-Record \
    --PermissionGroups.4.Permissions.1.Children.0.Children.3.Name 变更记录 \
    --PermissionGroups.4.Permissions.1.Children.0.Children.3.ParentKey  \
    --PermissionGroups.4.Permissions.1.Children.0.Children.3.Type 1 \
    --PermissionGroups.4.Permissions.1.Children.0.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.Children.0.DataRange 0 \
    --PermissionGroups.4.Permissions.1.Children.0.DataTo  \
    --PermissionGroups.4.Permissions.1.Children.0.DataType 0 \
    --PermissionGroups.4.Permissions.1.Children.0.Hide 0 \
    --PermissionGroups.4.Permissions.1.Children.0.IsChecked False \
    --PermissionGroups.4.Permissions.1.Children.0.Key SealManagement-Manage-Detail \
    --PermissionGroups.4.Permissions.1.Children.0.Name 查询印章 \
    --PermissionGroups.4.Permissions.1.Children.0.ParentKey  \
    --PermissionGroups.4.Permissions.1.Children.0.Type 2 \
    --PermissionGroups.4.Permissions.1.Children.1.Children.0.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.Children.1.Children.0.DataRange 0 \
    --PermissionGroups.4.Permissions.1.Children.1.Children.0.DataTo  \
    --PermissionGroups.4.Permissions.1.Children.1.Children.0.DataType 0 \
    --PermissionGroups.4.Permissions.1.Children.1.Children.0.Hide 1 \
    --PermissionGroups.4.Permissions.1.Children.1.Children.0.IsChecked False \
    --PermissionGroups.4.Permissions.1.Children.1.Children.0.Key SealManagement-Manage-Create-Template \
    --PermissionGroups.4.Permissions.1.Children.1.Children.0.Name 印章管理-可管理印章-新建印章-模版印章 \
    --PermissionGroups.4.Permissions.1.Children.1.Children.0.ParentKey  \
    --PermissionGroups.4.Permissions.1.Children.1.Children.0.Type 1 \
    --PermissionGroups.4.Permissions.1.Children.1.Children.1.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.Children.1.Children.1.DataRange 0 \
    --PermissionGroups.4.Permissions.1.Children.1.Children.1.DataTo  \
    --PermissionGroups.4.Permissions.1.Children.1.Children.1.DataType 0 \
    --PermissionGroups.4.Permissions.1.Children.1.Children.1.Hide 1 \
    --PermissionGroups.4.Permissions.1.Children.1.Children.1.IsChecked False \
    --PermissionGroups.4.Permissions.1.Children.1.Children.1.Key SealManagement-Manage-Create-Upload \
    --PermissionGroups.4.Permissions.1.Children.1.Children.1.Name 印章管理-可管理印章-新建印章-本地上传 \
    --PermissionGroups.4.Permissions.1.Children.1.Children.1.ParentKey  \
    --PermissionGroups.4.Permissions.1.Children.1.Children.1.Type 1 \
    --PermissionGroups.4.Permissions.1.Children.1.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.Children.1.DataRange 0 \
    --PermissionGroups.4.Permissions.1.Children.1.DataTo  \
    --PermissionGroups.4.Permissions.1.Children.1.DataType 0 \
    --PermissionGroups.4.Permissions.1.Children.1.Hide 0 \
    --PermissionGroups.4.Permissions.1.Children.1.IsChecked False \
    --PermissionGroups.4.Permissions.1.Children.1.Key CreateSeal \
    --PermissionGroups.4.Permissions.1.Children.1.Name 创建印章 \
    --PermissionGroups.4.Permissions.1.Children.1.ParentKey  \
    --PermissionGroups.4.Permissions.1.Children.1.Type 2 \
    --PermissionGroups.4.Permissions.1.Children.2.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.Children.2.DataRange 0 \
    --PermissionGroups.4.Permissions.1.Children.2.DataTo  \
    --PermissionGroups.4.Permissions.1.Children.2.DataType 0 \
    --PermissionGroups.4.Permissions.1.Children.2.Hide 0 \
    --PermissionGroups.4.Permissions.1.Children.2.IsChecked False \
    --PermissionGroups.4.Permissions.1.Children.2.Key ModifySeal \
    --PermissionGroups.4.Permissions.1.Children.2.Name 修改印章 \
    --PermissionGroups.4.Permissions.1.Children.2.ParentKey  \
    --PermissionGroups.4.Permissions.1.Children.2.Type 2 \
    --PermissionGroups.4.Permissions.1.Children.3.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.Children.3.DataRange 0 \
    --PermissionGroups.4.Permissions.1.Children.3.DataTo  \
    --PermissionGroups.4.Permissions.1.Children.3.DataType 0 \
    --PermissionGroups.4.Permissions.1.Children.3.Hide 0 \
    --PermissionGroups.4.Permissions.1.Children.3.IsChecked False \
    --PermissionGroups.4.Permissions.1.Children.3.Key CreateSealPolicy \
    --PermissionGroups.4.Permissions.1.Children.3.Name 分配印章管理人 \
    --PermissionGroups.4.Permissions.1.Children.3.ParentKey  \
    --PermissionGroups.4.Permissions.1.Children.3.Type 2 \
    --PermissionGroups.4.Permissions.1.Children.4.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.Children.4.DataRange 0 \
    --PermissionGroups.4.Permissions.1.Children.4.DataTo  \
    --PermissionGroups.4.Permissions.1.Children.4.DataType 0 \
    --PermissionGroups.4.Permissions.1.Children.4.Hide 0 \
    --PermissionGroups.4.Permissions.1.Children.4.IsChecked False \
    --PermissionGroups.4.Permissions.1.Children.4.Key DeleteSeal \
    --PermissionGroups.4.Permissions.1.Children.4.Name 删除印章 \
    --PermissionGroups.4.Permissions.1.Children.4.ParentKey  \
    --PermissionGroups.4.Permissions.1.Children.4.Type 2 \
    --PermissionGroups.4.Permissions.1.Children.5.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.Children.5.DataRange 0 \
    --PermissionGroups.4.Permissions.1.Children.5.DataTo  \
    --PermissionGroups.4.Permissions.1.Children.5.DataType 0 \
    --PermissionGroups.4.Permissions.1.Children.5.Hide 0 \
    --PermissionGroups.4.Permissions.1.Children.5.IsChecked False \
    --PermissionGroups.4.Permissions.1.Children.5.Key ApplySealOnce \
    --PermissionGroups.4.Permissions.1.Children.5.Name 单次用印审批 \
    --PermissionGroups.4.Permissions.1.Children.5.ParentKey  \
    --PermissionGroups.4.Permissions.1.Children.5.Type 2 \
    --PermissionGroups.4.Permissions.1.DataLabel 0 \
    --PermissionGroups.4.Permissions.1.DataRange 0 \
    --PermissionGroups.4.Permissions.1.DataTo  \
    --PermissionGroups.4.Permissions.1.DataType 0 \
    --PermissionGroups.4.Permissions.1.Hide 0 \
    --PermissionGroups.4.Permissions.1.IsChecked False \
    --PermissionGroups.4.Permissions.1.Key SealManagement \
    --PermissionGroups.4.Permissions.1.Name 印章管理 \
    --PermissionGroups.4.Permissions.1.ParentKey  \
    --PermissionGroups.4.Permissions.1.Type 1 \
    --PermissionGroups.5.GroupKey Template \
    --PermissionGroups.5.GroupName 模板中心 \
    --PermissionGroups.5.Hide 0 \
    --PermissionGroups.5.Permissions.0.Children.0.DataLabel 0 \
    --PermissionGroups.5.Permissions.0.Children.0.DataRange 0 \
    --PermissionGroups.5.Permissions.0.Children.0.DataTo  \
    --PermissionGroups.5.Permissions.0.Children.0.DataType 0 \
    --PermissionGroups.5.Permissions.0.Children.0.Hide 0 \
    --PermissionGroups.5.Permissions.0.Children.0.IsChecked False \
    --PermissionGroups.5.Permissions.0.Children.0.Key TemplateManagement-Query \
    --PermissionGroups.5.Permissions.0.Children.0.Name 查询模板 \
    --PermissionGroups.5.Permissions.0.Children.0.ParentKey  \
    --PermissionGroups.5.Permissions.0.Children.0.Type 1 \
    --PermissionGroups.5.Permissions.0.Children.1.DataLabel 0 \
    --PermissionGroups.5.Permissions.0.Children.1.DataRange 0 \
    --PermissionGroups.5.Permissions.0.Children.1.DataTo  \
    --PermissionGroups.5.Permissions.0.Children.1.DataType 0 \
    --PermissionGroups.5.Permissions.0.Children.1.Hide 0 \
    --PermissionGroups.5.Permissions.0.Children.1.IsChecked False \
    --PermissionGroups.5.Permissions.0.Children.1.Key OfficialFlowTemplateCollection \
    --PermissionGroups.5.Permissions.0.Children.1.Name 官方模板收藏 \
    --PermissionGroups.5.Permissions.0.Children.1.ParentKey  \
    --PermissionGroups.5.Permissions.0.Children.1.Type 1 \
    --PermissionGroups.5.Permissions.0.Children.2.DataLabel 0 \
    --PermissionGroups.5.Permissions.0.Children.2.DataRange 0 \
    --PermissionGroups.5.Permissions.0.Children.2.DataTo  \
    --PermissionGroups.5.Permissions.0.Children.2.DataType 0 \
    --PermissionGroups.5.Permissions.0.Children.2.Hide 0 \
    --PermissionGroups.5.Permissions.0.Children.2.IsChecked False \
    --PermissionGroups.5.Permissions.0.Children.2.Key TemplateManagement-Download \
    --PermissionGroups.5.Permissions.0.Children.2.Name 下载模板 \
    --PermissionGroups.5.Permissions.0.Children.2.ParentKey  \
    --PermissionGroups.5.Permissions.0.Children.2.Type 1 \
    --PermissionGroups.5.Permissions.0.Children.3.DataLabel 0 \
    --PermissionGroups.5.Permissions.0.Children.3.DataRange 0 \
    --PermissionGroups.5.Permissions.0.Children.3.DataTo  \
    --PermissionGroups.5.Permissions.0.Children.3.DataType 0 \
    --PermissionGroups.5.Permissions.0.Children.3.Hide 0 \
    --PermissionGroups.5.Permissions.0.Children.3.IsChecked False \
    --PermissionGroups.5.Permissions.0.Children.3.Key TemplateManagement-Create \
    --PermissionGroups.5.Permissions.0.Children.3.Name 创建模板 \
    --PermissionGroups.5.Permissions.0.Children.3.ParentKey  \
    --PermissionGroups.5.Permissions.0.Children.3.Type 1 \
    --PermissionGroups.5.Permissions.0.Children.4.DataLabel 0 \
    --PermissionGroups.5.Permissions.0.Children.4.DataRange 0 \
    --PermissionGroups.5.Permissions.0.Children.4.DataTo  \
    --PermissionGroups.5.Permissions.0.Children.4.DataType 0 \
    --PermissionGroups.5.Permissions.0.Children.4.Hide 0 \
    --PermissionGroups.5.Permissions.0.Children.4.IsChecked False \
    --PermissionGroups.5.Permissions.0.Children.4.Key DeleteFlowTemplates \
    --PermissionGroups.5.Permissions.0.Children.4.Name 删除模板 \
    --PermissionGroups.5.Permissions.0.Children.4.ParentKey  \
    --PermissionGroups.5.Permissions.0.Children.4.Type 2 \
    --PermissionGroups.5.Permissions.0.Children.5.DataLabel 0 \
    --PermissionGroups.5.Permissions.0.Children.5.DataRange 0 \
    --PermissionGroups.5.Permissions.0.Children.5.DataTo  \
    --PermissionGroups.5.Permissions.0.Children.5.DataType 0 \
    --PermissionGroups.5.Permissions.0.Children.5.Hide 0 \
    --PermissionGroups.5.Permissions.0.Children.5.IsChecked False \
    --PermissionGroups.5.Permissions.0.Children.5.Key ModifyFlowTemplate \
    --PermissionGroups.5.Permissions.0.Children.5.Name 编辑模板 \
    --PermissionGroups.5.Permissions.0.Children.5.ParentKey  \
    --PermissionGroups.5.Permissions.0.Children.5.Type 2 \
    --PermissionGroups.5.Permissions.0.DataLabel 0 \
    --PermissionGroups.5.Permissions.0.DataRange 0 \
    --PermissionGroups.5.Permissions.0.DataTo  \
    --PermissionGroups.5.Permissions.0.DataType 0 \
    --PermissionGroups.5.Permissions.0.Hide 0 \
    --PermissionGroups.5.Permissions.0.IsChecked False \
    --PermissionGroups.5.Permissions.0.Key TemplateManagement \
    --PermissionGroups.5.Permissions.0.Name 模板管理 \
    --PermissionGroups.5.Permissions.0.ParentKey  \
    --PermissionGroups.5.Permissions.0.Type 1
```

Output: 
```
{
    "Response": {
        "RoleId": "123456**89",
        "RequestId": " s19ksdjkkds****ldsjfkdfdf"
    }
}
```

**Example 2: 更新角色（不带权限树参数）**

更新一个自定义角色，并且不带权限信息

Input: 

```
tccli essbasic ChannelModifyRole --cli-unfold-argument  \
    --Agent.AppId  jsdk812kxkdfjks***k88123123 \
    --Agent.ProxyOrganizationOpenId test_org_openid \
    --Agent.ProxyOperator.OpenId test_openid \
    --RoleId 123456**89 \
    --Name xxx角色 \
    --Description 这是一个自定义角色
```

Output: 
```
{
    "Response": {
        "RoleId": "123456**89",
        "RequestId": " s19ksdjkkds****ldsjfkdfdf"
    }
}
```

