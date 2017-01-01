<div align=center><img src="https://github.com/youlookwhat/CloudReader/blob/master/file/title.png""/></div>

## Detail Introduction
　　网易云音乐于2013年4月23日正式发布，是一款主打发现和分享，带有浓厚社交基因的网络音乐产品。相信用过的人都知道它给人的体验是极好的，“听得越多，推荐越准”
　　
## 效果图
- **干货**

<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_gank_00.png"></img>
<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_gank_01.png"></img>
<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_gank_02.png"></img>
<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_gank_03.png"></img>
<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_gank_04.png"></img>

- **电影**

<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_movie_01.png"></img>
<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_movie_02.png"></img>
<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_movie_03.png"></img>

- **书籍**

<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_book_01.png"></img>
<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_book_02.png"></img>
<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_book_03.png"></img>

- **抽屉界面**

<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_menu_01.png"></img>
<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_menu_02.png"></img>
<img width="160" height=“274” src="https://github.com/youlookwhat/CloudReader/blob/master/file/page_menu_03.png"></img>
　　
　　
## 模块分析
### 干货区（gank.io）
> API使用的是动听（轮播图）和代码家的Gank.Io。

- **每日推荐：** 干货集中营推送的每日内容，包括每天一个妹子图，相关Android、IOS等其他干货。每天第12：30之后更新，因为双休不更新所以内容缓存三天网络取不到就取缓存。

- **福利：** Glide加载图片，点击查看大图，支持双指缩放，一下可查看列表的所有图片，再也不用逐个点击每张图啦。

- **干货订制：** 可以筛选自己喜欢干货的类别，有全部、IOS、App、前端、休息视频和拓展资源。

- **大安卓：** 显示安卓的全部资讯。支持下拉刷新方便查看最新的资源。


### 电影区（豆瓣）
> API是豆瓣提供的，因为限制了每个ip每分钟请求的次数，所以请酌情使用，由此带来的不便请见谅。

 - **电影热映区：** 每日更新，展示最新上映的电影热度排行榜。
 - **豆瓣电影Top250：** 豆瓣高分电影集锦，让你放心找好片~

### 书籍区（豆瓣）
> 使用的是豆瓣的搜索API。更多订制内容由于时间原因第一版还未添加，第二版会加上。

 - **综合：** 检索豆瓣综合类的书籍并展示。
 - **文学：** 检索豆瓣文学类的书籍并展示。
 - **生活：** 检索豆瓣生活类的书籍并展示。

### 抽屉界面
> 完全仿网易云音乐抽屉界面，包括诸多细节如透明标题栏，背景透明度，水波纹颜色等。

 - **项目主页：**展示项目介绍信息，及内容说明，可以分享给你的好友哦。
 - **扫码下载：**扫码即可下载App，帮助您快速试用~
 - **问题反馈：**常见问题归纳，反馈地方，联系方式都在这里哦！
 - **关于云阅：**更新日志在这里可见，主人是利用工作外时间做的，周期较长，满意的小伙伴给个Star吧，这将是我继续迭代的动力，谢谢~


## 功能特性
 - 高仿网易云音乐UI，追求细节，执着于1dp与1px的差距。
 - 整体采用Material Desgin设计风格，尽量遵循其设计规范。
 - 项目``BaseActivity``和``BaseFragment``皆基于``DataBinding``，且使用``fragment``懒加载模式，节省内存资源，代码结构清晰。
 - 加载动画和缓存策略都仿网易云音乐，不可以说一模一样但基本是这个套路。列表使用的是``RecyclerView``基于``DataBinding``的``BaseHolder``,使用方便，高效，简洁。
 - 电影详情页是仿网易云音乐的歌单详情页做的，并封装成基类，方便使用。效果有转场动画，透明状态栏，滑动title渐变色等，几乎和歌单详情页一模一样。
 - 书籍类数据展示使用的是``SwipeRefreshLayout``刷新控件结合``RecyclerView``的方式，支持一般的列表、GridView和瀑布流的上拉加载的使用。