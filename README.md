# log4mongo-netcore
Log4net MongoDB .net core version
<br/>
版本来源：
<br/>
https://github.com/log4mongo/log4mongo-net
<br/>
调整对.net core 2.2版本的支持
<br/>
增加了对CollectionName 日期命名的的定义
<br/>
<!--定义输出到MongoDB中,循环创建日志文件，以日期命名-->
<br/>
<appender name="MongoDBAppender" type="Log4Mongo.MongoDBAppender, Log4Mongo">
	<br/>
   <!--mongodb://ip:port/datebasename-->
	<br/>
  <connectionString value="mongodb://localhost:27017/logs_log4net" />
	<br/>
  <!--CollectionName 支持自定义命名及日期yyyyMMdd、yyyy、yyyyMM格式输出为logs20201125、logs2020、logs202011-->
	<br/>
  <CollectionName value="yyyyMMdd"/>
	<br/>
  <newCollectionMaxSize value='50MB' />
	<br/>
  <newCollectionMaxDocs value='100000' />    
	<br/>
</appender>
<br/>
