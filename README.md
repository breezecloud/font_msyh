# 前言 Preface
    你有没有遇到过嵌入式系统使用python写程序时想显示一些中文字体，但发现当前环境没有中文字体？当然你可以找一个中文字文件体复制到本地，在使用该字体。但我的解决方案是打包一个中文字体到pypi，然后使用pip安装这个字体并使用。这不是我的发明，是看了https://pypi.org/project/fonts/ 这个项目了解了这样的用法，可以避免到处找字体文件。

Have you ever encountered a situation where you wanted to display some Chinese fonts when writing programs in python for an embedded system, but found that there were no Chinese fonts in the current environment? Of course, you can find a Chinese character file font, copy it to your local device, and then use that font. But my solution is to package a Chinese font to pypi, and then install and use this font using pip. This is not my invention, is to look at the https://pypi.org/project/fonts/ understand the usage of this, the project can avoid looking for font files.

# font-msyh 
这是微软雅黑字体文件，版本0.75。该字体使用需要Python Fonts模块（https://pypi.org/project/fonts/）

Microsoft YaHei font file, version 0.75. This font has been repackaged for the Python Fonts module: https://pypi.org/project/fonts/ 

# install
pip install font-msyh
source code https://github.com/breezecloud/font_msyh

# example
```
from PIL import Image, ImageDraw, ImageFont
from fonts.ttf import msyh as UserFont
# 创建一个空白图像
image = Image.new('RGB', (400, 200), color='white')
draw = ImageDraw.Draw(image)
# 加载 TTF 字体文件，指定字体大小
# 替换为你的 TTF 文件路径
font = ImageFont.truetype(UserFont, size=36)
# 在图像上绘制文本
draw.text((50, 80), "Hello, 世界!", font=font, fill='black')
# 保存图像
image.save('output.png')
```
