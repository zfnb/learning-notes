### step 在animation中在过渡函数曲线的位置，填上它，过渡动画就会以跳转的形式过渡
- steps(整个动画跳动次数，过渡形式)
- 过渡形式有两种：start:保留下一帧转态，直到动画结束，所以第一帧动画看不到
                 ***end***:保留当前状态，直到这段动画结束，由于倒数第二帧动画保留倒数第二帧的状态，所以最后一帧动画看不到，可以配合forward保留最后一帧转态
- step-start === steps(1,start) step-end === steps(1,end) 
## transfrom:
### rotate3d(x,y,z,deg) x,y,z为矢量方向，也是旋转轴    
### scalex() scaley() scalez() 将坐标轴x/y刻度变为原来的倍数，（雁过留声）保留变化痕迹，（旋转后依然保留）        
### skew(x角度，y角度) 改变坐标轴倾斜，同时拉伸坐标轴，设置x角度，倾斜y轴，设置y角度，倾斜x轴。     