# show create table sa_user\G; // 显示建表脚本 linux 环境下测试可用
# 1. 建表时添加注释.
CREATE TABLE `event_table` (  
  `event_id` varchar(32) NOT NULL DEFAULT '' COMMENT '这个属性是ID号',  
  `EVENT_DATE` datetime DEFAULT NULL,  
  `title` varchar(45) DEFAULT NULL,  
  PRIMARY KEY (`event_id`)  
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COMMENT='这只是一个测试的表而已'"  

# 2. 建表之后添加注释
alter table event_table modify column event_id varchar(32) comment '这个属性是ID号';  

# 3. 查看注释(只显示列Column的Comment)
show full columns from event_table;  

# 4. 查看表的所有注释(显示表Table的Comment)
SHOW CREATE TABLE event_table;
