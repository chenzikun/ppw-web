spec link: http://192.168.1.71/web3.2.8/#p=发布


**修改接口：**

[业务大厅查询]
(http://192.168.1.200:8008/index.php?title=OpportunityService#sitingTransferQuery_xwWeb)

[业务大厅搜索]
(http://192.168.1.200:8008/index.php?title=OpportunityService#searchSitingTransfer_xwWeb)

[商机详情]
(http://192.168.1.200:8008/index.php?title=OpportunityService#getInfo)

[案例列表查询]
(http://192.168.1.200:8008/index.php?title=ExampleService#webQueryExample)

[案例列表搜索]
(http://192.168.1.200:8008/index.php?title=ExampleService#searchExample_.28V2.7_.E5.BA.9F.29)

[发布招商]
(http://192.168.1.200:8008/index.php?title=Client:BrandService#set)

[发布商机]
(http://192.168.1.200:8008/index.php?title=OpportunityService#add)

[发布外网](http://192.168.1.200:8008/index.php?title=Client:PublishWebsiteService#add)

[中介同行](http://192.168.1.200:8008/index.php?title=Client:BlackListService#addIntermediaryPhone)

------------------------------------------------------------------------------------------------------------------------

**新加接口：**

[客户短信记录列表]
(http://192.168.1.200:8008/index.php?title=Client:SmsService#listSendMessage_.EF.BC.88.E6.96.B0.EF.BC.89)

[根据手机号码或用户名，查询用户信息]
(http://192.168.1.200:8008/index.php?title=UserService#query)

[添加案例后服务]
(http://192.168.1.200:8008/index.php?title=ExampleAfterService#add)

[修改案例后服务]
(http://192.168.1.200:8008/index.php?title=ExampleAfterService#update)

[获取案例后服务列表]
(http://192.168.1.200:8008/index.php?title=ExampleAfterService#list)

[案例后服务详情]
(http://192.168.1.200:8008/index.php?title=ExampleAfterService#get)

[删除案例后服务]
(http://192.168.1.200:8008/index.php?title=ExampleAfterService#delete)

[添加各类备注]
(http://192.168.1.200:8008/index.php?title=OppRemarkService#add_2)

[获取相关备注列表]
(http://192.168.1.200:8008/index.php?title=OppRemarkService#getRelatedList)

[获取备注图片信息]
(http://192.168.1.200:8008/index.php?title=OppRemarkService#getPhotoList)

[网站留言资源列表]
(http://192.168.1.200:8008/index.php?title=Client:ApplyService#list_.EF.BC.88.E6.96.B0.EF.BC.89)

[我的业务列表]
(http://192.168.1.200:8008/index.php?title=BusinessService#getList_.EF.BC.88.E6.96.B0.EF.BC.89)          DELETEED

http://192.168.1.200:8008/index.php?title=BusinessService#search_.EF.BC.88.E6.96.B0.EF.BC.89               DELETEED

http://192.168.1.200:8008/index.php?title=BusinessService#getOfferAndReception_.EF.BC.88.E6.96.B0.EF.BC.89

http://192.168.1.200:8008/index.php?title=BusinessService#getSameMobileInfo_.EF.BC.88.E6.96.B0.EF.BC.89              DELETEED



http://192.168.1.200:8008/index.php?title=Client:SmsService#listReplyMessage_.EF.BC.88.E6.96.B0.EF.BC.89 


------------------------------------------------------------------------------------------------------------------------------------

**内部调整的代码：**

1.权限控制，SQL数据

2.推荐接口，自动产生“推荐客户备注”数据，归类为，业务备注 数据

3.原有的涉及到：商机备注，服务记录，服务备注 写入的接口，调整为新表结构

4.上传案例视频，文件格式和视频编码格式限制     DELETEED
http://192.168.1.200:8008/index.php?title=Upload#.E4.B8.8A.E4.BC.A0.E8.A7.86.E9.A2.91.E6.8E.A5.E5.8F.A3

5.放弃业务选项及功能调整，放弃任务自动添加备注功能修改
http://192.168.1.200:8008/index.php?title=BusinessService#abort

6.前端控制，举报商机信息后，调用备注接口，加一条举报信息系统备注
