# font_msyh
Microsoft YaHei font file, version 0.75. This font has been repackaged for the Python Fonts module: https://pypi.org/project/fonts/ 
# install 
pip install font-msyh
# usage
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
