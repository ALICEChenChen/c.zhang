
# the design of database in market website

the tables' structure(Mysql)
```markdown

SET FOREIGN_KEY_CHECKS=0;

-- ----------------------------
-- Table structure for `t_admin`
-- ----------------------------
DROP TABLE IF EXISTS `t_admin`;
CREATE TABLE `t_admin` (
  `userId` int(11) NOT NULL,
  `userName` varchar(55) DEFAULT NULL,
  `userPw` varchar(55) DEFAULT NULL,
  PRIMARY KEY (`userId`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;



-- ----------------------------
-- Table structure for `t_catelog`
-- ----------------------------
DROP TABLE IF EXISTS `t_catelog`;
CREATE TABLE `t_catelog` (
  `catelog_id` int(11) NOT NULL,
  `catelog_name` varchar(88) DEFAULT NULL,
  `catelog_del` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`catelog_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;



-- ----------------------------
-- Table structure for `t_gonggao`
-- ----------------------------
DROP TABLE IF EXISTS `t_gonggao`;
CREATE TABLE `t_gonggao` (
  `gonggao_id` int(11) NOT NULL,
  `gonggao_title` varchar(50) DEFAULT NULL,
  `gonggao_content` varchar(5000) DEFAULT NULL,
  `gonggao_data` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`gonggao_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;


-- ----------------------------
-- Table structure for `t_goods`
-- ----------------------------
DROP TABLE IF EXISTS `t_goods`;
CREATE TABLE `t_goods` (
  `goods_id` int(11) NOT NULL,
  `goods_name` varchar(88) DEFAULT NULL,
  `goods_miaoshu` varchar(5000) DEFAULT NULL,
  `goods_pic` varchar(50) DEFAULT NULL,
  `goods_shichangjia` int(11) DEFAULT NULL,
  `goods_tejia` int(11) DEFAULT NULL,
  `goods_isnottejia` varchar(50) DEFAULT NULL,
  `goods_isnottuijian` varchar(50) DEFAULT NULL,
  `goods_catelog_id` int(11) DEFAULT NULL,
  `goods_Del` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`goods_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;


-- ----------------------------
-- Table structure for `t_liuyanban`
-- ----------------------------
DROP TABLE IF EXISTS `t_liuyanban`;
CREATE TABLE `t_liuyanban` (
  `id` int(11) NOT NULL,
  `neirong` varchar(4000) DEFAULT NULL,
  `liuyanshi` varchar(55) DEFAULT NULL,
  `userId` int(11) DEFAULT NULL,
  `huifu` varchar(4000) DEFAULT NULL,
  `huifushi` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;


-- ----------------------------
-- Table structure for `t_order`
-- ----------------------------
DROP TABLE IF EXISTS `t_order`;
CREATE TABLE `t_order` (
  `id` int(11) NOT NULL,
  `bianhao` varchar(88) DEFAULT NULL,
  `xiadanshi` varchar(50) DEFAULT NULL,
  `userName` varchar(255) DEFAULT NULL,
  `userRealname` varchar(255) DEFAULT NULL,
  `userTel` varchar(255) DEFAULT NULL,
  `songhuodizhi` varchar(50) DEFAULT NULL,
  `fukuanfangshi` varchar(50) DEFAULT NULL,
  `jine` int(11) DEFAULT NULL,
  `zhuangtai` varchar(50) DEFAULT NULL,
  `userId` int(11) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;


-- ----------------------------
-- Table structure for `t_orderitem`
-- ----------------------------
DROP TABLE IF EXISTS `t_orderitem`;
CREATE TABLE `t_orderitem` (
  `orderItem_id` int(11) NOT NULL,
  `order_id` int(11) DEFAULT NULL,
  `goods_id` int(11) DEFAULT NULL,
  `goods_quantity` int(11) DEFAULT NULL,
  PRIMARY KEY (`orderItem_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;


-- ----------------------------
-- Table structure for `t_renyuan`
-- ----------------------------
DROP TABLE IF EXISTS `t_renyuan`;
CREATE TABLE `t_renyuan` (
  `id` int(11) NOT NULL,
  `xingming` varchar(200) DEFAULT NULL,
  `xingbie` varchar(50) DEFAULT NULL,
  `nianling` int(11) DEFAULT NULL,
  `xueli` varchar(50) DEFAULT NULL,
  `loginname` varchar(50) DEFAULT NULL,
  `loginpw` varchar(50) DEFAULT NULL,
  `del` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;


-- ----------------------------
-- Table structure for `t_tupian`
-- ----------------------------
DROP TABLE IF EXISTS `t_tupian`;
CREATE TABLE `t_tupian` (
  `id` int(11) NOT NULL DEFAULT '0',
  `xinwen_id` int(11) DEFAULT NULL,
  `jieshao` varchar(3000) DEFAULT NULL,
  `fujian` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;


-- ----------------------------
-- Table structure for `t_user`
-- ----------------------------
DROP TABLE IF EXISTS `t_user`;
CREATE TABLE `t_user` (
  `user_id` int(11) NOT NULL,
  `user_name` varchar(50) DEFAULT NULL,
  `user_pw` varchar(77) DEFAULT NULL,
  `user_realname` varchar(50) DEFAULT NULL,
  `user_sex` varchar(55) DEFAULT NULL,
  `user_age` int(11) DEFAULT NULL,
  `user_address` varchar(55) DEFAULT NULL,
  `user_tel` varchar(50) DEFAULT NULL,
  `user_card` varchar(66) DEFAULT NULL,
  `user_del` varchar(55) DEFAULT NULL,
  PRIMARY KEY (`user_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;



-- ----------------------------
-- Table structure for `t_xieyi`
-- ----------------------------
DROP TABLE IF EXISTS `t_xieyi`;
CREATE TABLE `t_xieyi` (
  `id` int(11) NOT NULL,
  `neirong` varchar(3000) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- ----------------------------
-- Table structure for `t_xinwen`
-- ----------------------------
DROP TABLE IF EXISTS `t_xinwen`;
CREATE TABLE `t_xinwen` (
  `id` int(11) NOT NULL,
  `biaoti` varchar(200) DEFAULT NULL,
  `neirong` varchar(3000) DEFAULT NULL,
  `fujian` varchar(255) DEFAULT NULL,
  `shijian` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;



-- ----------------------------
-- Table structure for `t_zuihous`
-- ----------------------------
DROP TABLE IF EXISTS `t_zuihous`;
CREATE TABLE `t_zuihous` (
  `id` int(11) NOT NULL DEFAULT '0',
  `userId` int(11) DEFAULT NULL,
  `guanjianzi` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;


```


