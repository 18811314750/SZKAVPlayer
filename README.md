# SZKAVPlayer
iOS在线音乐播放SZKAVPlayer（基于AVPlayer的封装） 提供播放，暂停，上一首，下一首接口,   实现自动切换歌曲和背景图片的功能， 并用代理方法返回当前时间，总共时间，歌曲进度等。

SZKAVPlayer 详情文档 简书 http://www.jianshu.com/p/4e0ac2898de0



初始化player时传入歌曲的网址数组跟歌曲的背景图片数组便可实现当前歌曲播放结束后，自动播放下一首并切换player的背景图片（支持本地图片和网络图片）

/**
 *  初始化SZKAVPlayer
 *
 *  @param frame  AVPlayerLayer的frame
 *  @param urlArr 歌曲网址的数组
 *  @param urlArr 歌曲背景图片网址的数组
 *
 *  @return   SZKAVPlayer
 */

-(instancetype)initWithFrame:(CGRect)frame
               andSongUrlArr:(NSArray *)urlArr
             andSongImageArr:(NSArray *)imageArr;


player的其他操作调用SZKAVPlayer.h中相关的API即可

/**
 *  开始播放
 */
 
-(void)startPlay;

/**
 *  暂停播放
 */
 
-(void)puasePlay;

/**
 *  播放下一首
 */
 
-(void)nextSong;

/**
 *  播放上一首
 */
 
-(void)lastSong;

