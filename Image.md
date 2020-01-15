# egret引擎中, bitmap,bitmapdata,texture的联系和区别
引用关系:  
bitmap<-texture<-bitmapdata<-source(Image)  

bitmapdata 引用了一个Image和一个webgl纹理, 需要释放内存时要将Image和webgl纹理都释放掉.

texture 引用了bitmapdata,暴露了一些纹理数据.

bitmap 引用了texture,将纹理显示出来.