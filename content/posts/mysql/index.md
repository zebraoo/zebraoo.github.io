+++
title = 'MySql相关知识点'
date = 2023-10-19
tags= ['MySql']
+++

# Mysql表里将某个字段的所有数据的中文字符串的第一个汉字转成拼音字母并生成新的字段
 ``` sql

-- 创建新字段用于存储拼音
ALTER TABLE your_table ADD COLUMN pinyin_field VARCHAR(255);

-- 更新新字段的值
UPDATE your_table
SET pinyin_field = (
  SELECT
    ELT(
      INTERVAL(CONV(HEX(LEFT(CONVERT(original_field USING gbk), 1)), 16, 10),
        0xB0A1,0xB0C5,0xB2C1,0xB4EE,0xB6EA,0xB7A2,0xB8C1,0xB9FE,0xBBF7, 
        0xBFA6,0xC0AC,0xC2E8,0xC4C3,0xC5B6,0xC5BE,0xC6DA,0xC8BB,
        0xC8F6,0xCBFA,0xCDDA,0xCEF4,0xD1B9,0xD4D1),
      'A','B','C','D','E','F','G','H','J','K','L','M','N','O','P','Q','R','S','T','W','X','Y','Z'
    )
  FROM dual
);

-- 请替换 your_table、original_field 和 pinyin_field 为您的实际表名和字段名。这个SQL查询会为表中的每行记录的 original_field 字段的第一个汉字提取拼音并存储在 pinyin_field 中。

UPDATE region2022
SET pinyin_prefix = (
  SELECT
    ELT(
      INTERVAL(CONV(HEX(LEFT(CONVERT(`name` USING gbk), 1)), 16, 10),
        0xB0A1,0xB0C5,0xB2C1,0xB4EE,0xB6EA,0xB7A2,0xB8C1,0xB9FE,0xBBF7, 
        0xBFA6,0xC0AC,0xC2E8,0xC4C3,0xC5B6,0xC5BE,0xC6DA,0xC8BB,
        0xC8F6,0xCBFA,0xCDDA,0xCEF4,0xD1B9,0xD4D1),
      'A','B','C','D','E','F','G','H','J','K','L','M','N','O','P','Q','R','S','T','W','X','Y','Z'
    )
  FROM dual
);

 ```