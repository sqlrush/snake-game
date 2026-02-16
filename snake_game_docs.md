# 贪吃蛇游戏开发全过程

## 1. 创建游戏代码

### 代码文件
路径：`/Users/yingjiewang/.openclaw/workspace/snake_game.py`

### 核心代码
```python
import pygame
import time
import random

# 初始化
pygame.init()

# 颜色
WHITE = (255, 255, 255)
YELLOW = (255, 255, 102)
BLACK = (0, 0, 0)
RED = (213, 50, 80)
GREEN = (0, 255, 0)
BLUE = (50, 153, 213)

# 屏幕尺寸
WIDTH = 600
HEIGHT = 400

screen = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption('贪吃蛇游戏')

# 时钟
clock = pygame.time.Clock()

# 蛇的大小
SNAKE_BLOCK = 10

# 速度
SNAKE_SPEED = 15
```

## 2. 安装 pygame 依赖

```bash
# 安装 pygame
pip3 install pygame
```

输出：
```
Collecting pygame
  Downloading pygame-2.6.1-cp39-cp39-macosx_11_0_arm64.whl (12.4 MB)
Installing collected packages: pygame
Successfully installed pygame-2.6.1
```

## 3. Git 初始化与提交

```bash
# 进入工作目录
cd /Users/yingjiewang/.openclaw/workspace

# 添加文件到暂存区
git add snake_game.py

# 提交代码
git commit -m "添加贪吃蛇游戏"
```

输出：
```
[master（根提交） 001347e] 添加贪吃蛇游戏
 1 file changed, 142 insertions(+)
 create mode 100644 snake_game.py
```

## 4. 创建 GitHub 仓库并推送

```bash
# 创建公开仓库
gh repo create snake-game --public --source=. --description "Python Pygame 贪吃蛇游戏"

# 推送代码到远程
git push -u origin master
```

输出：
```
To https://github.com/sqlrush/snake-game.git
 * [new branch]      master -> master
分支 'master' 设置为跟踪 'origin/master'。
```

## 5. 最终结果

- **仓库地址**: https://github.com/sqlrush/snake-game
- **代码文件**: https://github.com/sqlrush/snake-game/blob/master/snake_game.py

## 6. 运行游戏

```bash
python3 /Users/yingjiewang/.openclaw/workspace/snake_game.py
```

或直接在 PyCharm 中打开运行：

```bash
open -a "PyCharm" /Users/yingjiewang/.openclaw/workspace/snake_game.py
```

## 游戏操作说明

- 🎮 方向键控制蛇的移动
- 🍎 吃到红色食物变长
- ❌ 撞墙或撞自己游戏结束
- 按 Q 退出，C 重新开始
