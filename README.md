# log4mongo-netcore
Log4net MongoDB .net core version
版本来源：
https://github.com/log4mongo/log4mongo-net
调整对.net core 2.2版本的支持
增加了对CollectionName 日期命名的的定义
<!--定义输出到MongoDB中,循环创建日志文件，以日期命名-->
<appender name="MongoDBAppender" type="Log4Mongo.MongoDBAppender, Log4Mongo">
   <!--mongodb://ip:port/datebasename-->
  <connectionString value="mongodb://localhost:27017/logs_log4net" />
  <!--CollectionName 支持自定义命名及日期yyyyMMdd、yyyy、yyyyMM格式输出为logs20201125、logs2020、logs202011-->
  <CollectionName value="yyyyMMdd"/>
  <newCollectionMaxSize value='50MB' />
  <newCollectionMaxDocs value='100000' />      
</appender>
