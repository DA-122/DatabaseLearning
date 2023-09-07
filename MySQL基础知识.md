## SQL解析过程


## SELECT语句执行过程
一个SELECT语句可以总结为以下句式：

`SELECT XXX FROM XXX WHERE XXX GROUP BY XXX HAVING XXX ORDER BY XXX LIMIT XXX;`

* 1.FROM 语句，负责把数据表文件加载到内存去；
* 2.WHERE 语句，会把1表中的数据进行过滤，取出符合条件的记录，生成一张临时表(1)；
* 3.SELECT 语句， 
  * 如果没有GROUP BY，会直接根据字段对临时表整列SELECT，得到临时表(2)；
  * 如果有GROUP BY，会将临时表1切分成多个临时表，分别执行SELECT，且只取表中的第一条记录，然后再形成新的临时表(2)；
* 4.HAVING 语句，只能用在GROUP BY之后，HAVING是对SELECT之后的临时表中的数据进行过滤，因此SELECT后面没有的字段不能用在HAVING之后。
* 5.ORDER BY 语句，对以上临时表(2)按照字段进行排序；
* 6.LIMIT 语句，取排序后的前多少个元素。