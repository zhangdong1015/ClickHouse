# Final 
 - ClickHouse 会在返回结果之前完全合并数据，从而执行给定表引擎合并期间发生的所有数据转换.
 - select 语句+final 的话，会对表的 order 字段进行排序去重。注意主键要加上分区字段（虽然跨分区不会去重，但 select 会合并结果)
 -  join table  final 这样不会去重，join (select * from table final)这样才能去重
