# HCTF_New_Love_Song

## A challenge about Wav-Steganography

watermarking an image into an audio file

不知道各位还记不记得去年HCTF的图片隐写题，去年的大一通信小学弟今年已经大二了。
他从课堂上学会了音频隐写，~~并选了大家（wo）LP的一首歌准备在双11送给大家（虽然没几个人开到）~~

## __解题分析：__

题目后来也放过 __hint: concentrate on the waveform 注意波形图__
用 __Audacity__ 打开 __new_love_song.wav__ ,基本近似于一种矩形:
![new_love_song](http://olqhuq6wn.bkt.clouddn.com/HCTF_1.png  "new_love_song")
而正常的音频波形往往都是高低起伏的:
![new_love_song](http://olqhuq6wn.bkt.clouddn.com/HCTF_3.png  "new_love_song")
所以我们就把波放大，能够发现：
![new_love_song](http://olqhuq6wn.bkt.clouddn.com/HCTF_2.png  "new_love_song")
相隔特定的距离 就会出现一段直线。接触过的人肯定知道，直线波就是某一特定的值
能够猜测 肯定有东西藏在其中，尝试提取出来，发现是一串01串 长度可开方 ，又是熟悉的转换二维码，扫描get flag
