<div align="center">
    <h2>crawLdb - 豆瓣数据爬虫和数据文本分析平台</h2>
    <img src="./images/header.jpg"/>
    <div align="center">
    </div> 
</div>


> 目前仅针对豆瓣平台进行分析，~~后续会加入对哔哩哔哩平台分析功能（有空再做吧，操）~~
>

#### 功能

- 实时爬取豆瓣网站电影评论、电影详情信息
- 自动化对电影评论+详情进行主题建模和情感分析
- 对电影评论+电影详情进行信息管理等等
- 对用户信息进行增删改查等等
- 自定义代理池爬取
- 对日志信息进行增删改查等等
- 2FA登录认证

> 因为数据量太大（有100w+的评论数据和2k部电影信息），所以数据库就不放在Git上了，有需要的可以自己重新爬取下

#### 技术栈

##### 前端

- React
- Ant Design全家桶
- L7Plot 地理空间可视化图表库

设计语言：TypeScript (EX: JavaScript)

测试框架：Mock.js

##### 后端

- PyOTP (Google Authentication)
- Django Rest Framework (DRF)
  
- 数据库：MySQL
- 数据缓存：Redis

#### 爬虫系统使用说明

1. 进入豆瓣 https://movie.douban.com/explore，选择需要爬取的电影标签
2. 进入平台系统，爬虫系统->创建爬虫->填写对应的电影标签和任务详情，新建爬虫即可

![](./images/20.jpg)

![](./images/21.jpg)

**演示过程**

![](./images/19.gif)

**爬虫系统数据格式**

```json
{
		"id": 559,
		"movie_id": "33454816",
		"movie_name": "我是如何成为超级英雄的 Comment je suis devenu super-héros",
		"movie_release_time": "(2020)",
		"movie_maker": "Douglas Attal",
		"movie_acter": "皮奥·马麦,Benoît Poelvoorde,斯万·阿劳德,LEÏLA BEKHTI,VIMALA PONS",
		"movie_type": "动作,科幻",
		"movie_times": "97分钟",
		"movie_platform": "douban",
		"movie_country": "法国 France",
		"movie_language": "法语 French",
		"movie_vote_total": "5.4",
		"movie_vote_people": "794",
		"movie_vote_star5": "2.6%",
		"movie_vote_star4": "8.8%",
		"movie_vote_star3": "51.7%",
		"movie_vote_star2": "28.1%",
		"movie_vote_star1": "8.8%",
		"movie_desc": "2021年巴黎。超级英雄完美融入社会。一种可以赋予普通人超能力的神秘毒品在城市中传播。由于这类事件不断增多，莫罗中尉和沙尔茨曼被指派前去调查真相。他们将与两位资深治安会成员蒙特·卡洛和卡莉丝塔联手，竭尽全力遏制毒品的扩散。然而莫罗的过去重新浮出水面，事情变得十分棘手······",
		"movie_short_comment": "全部 220 条",
		"movie_long_comment": "全部 4 条",
		"movie_platform_comment": null,
		"taskname": "miaomiaomioa",
		"comments": [
			{
				"id": 72289,
				"comment_name": "Sanitya",
				"comment_pageurl": "https://www.douban.com/people/Vine0109/",
				"comment_id": "3140646335",
				"comment_rank": "0",
				"comment_content": "有事吗",
				"comment_date": "2021-12-08T13:30:23Z",
				"comment_movie_id": "33454816",
				"comment_platform": "douban",
				"taskname": "miaomiaomioa"
			},
			{
				"id": 72290,
				"comment_name": "爱吃菜的小豆豆",
				"comment_pageurl": "https://www.douban.com/people/bihailantianmen/",
				"comment_id": "3951794307",
				"comment_rank": "0",
				"comment_content": "本身很好的题材，为什么拍的却这么烂，这么无聊？完全看不下去了",
				"comment_date": "2023-10-04T16:03:40Z",
				"comment_movie_id": "33454816",
				"comment_platform": "douban",
				"taskname": "miaomiaomioa"
			},
			{
				"id": 72306,
				"comment_name": "? J@,  @L?",
				"comment_pageurl": "https://www.douban.com/people/149292382/",
				"comment_id": "3067848090",
				"comment_rank": "0",
				"comment_content": "这节奏跟故事，感觉适合连续剧多过电影吖！",
				"comment_date": "2021-10-09T21:58:02Z",
				"comment_movie_id": "33454816",
				"comment_platform": "douban",
				"taskname": "miaomiaomioa"
			},
        ]
}
```

#### 项目截图

##### 首页

![](./images/1.jpg)

##### 登录页面

![](./images/15.jpg)

##### 登陆页面（2FA）

![](./images/16.jpg)

##### 爬虫页面

![](./images/17.jpg)

##### 爬虫页面（新建任务）

![](./images/3.jpg)

##### 爬虫页面（新建任务）

![](./images/2.jpg)

##### 爬虫页面（任务爬取状态）

![](./images/18.jpg)

##### 评论页面

![](./images/4.jpg)

##### 情感分析页面

![](./images/7.jpg)

##### 用户管理页面

![](./images/10.jpg)

##### 用户管理页面（用户新增）

![](./images/11.jpg)

##### 用户管理页面（用户详情）

![](./images/12.jpg)

##### 系统管理页面

![](./images/13.jpg)

##### 系统日志页面

![](./images/14.jpg)

#### 版权许可说明

```
GNU GENERAL PUBLIC LICENSE
Version 3, 29 June 2007

Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
Everyone is permitted to copy and distribute verbatim copies
of this license document, but changing it is not allowed.
```
