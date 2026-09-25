# 把你的头像放在这个文件夹里

## 怎么做

**只需一步**：把照片拷进这个文件夹，命名成 **`me.jpg`**，然后推送到 GitHub：

```bash
git add .
git commit -m "update: 更换头像"
git push
```

代码已经配好了，**不用改任何文件**，约 1 分钟后线上自动生效。

## 效果

头像是**圆形**的。代码里用了 `aspect-ratio:1/1` + `object-fit:cover`，
所以**任何比例的照片都会被自动裁成正圆**（而不是被压成椭圆），你不用自己先裁图。

照片还没放进来时，页面会自动回退显示原来的占位插画，**不会出现裂图**。

## 照片要求

| 项目 | 建议 |
|---|---|
| 比例 | 正方形最好；竖版 / 横版也能用（自动取中间部分） |
| 尺寸 | 600×600 以上（页面显示约 270px，留 2 倍给高分屏） |
| 格式 | `.jpg` 照片首选；要透明背景用 `.png`；`.webp` 体积最小 |
| 体积 | 控制在 **300 KB** 以内，加载更快 |

> 别直接放手机原图（可能 5 MB 以上），先用系统自带工具或
> <https://squoosh.app> 压缩一下。

裁切时注意**把脸放在画面正中间**，因为 `object-fit:cover` 取的是中心区域。

## 如果文件名不叫 me.jpg

比如你想用 `me.png`，改 `index.html` 里这一行的 `src` 就行：

```html
<img style="width:85%;max-width:85%;aspect-ratio:1/1;object-fit:cover;border-radius:50%;"
     alt="【你的照片】"
     src="images/avatar/me.jpg"
     onerror="this.onerror=null;this.src='images/template/avatar.svg';">
```

## 注意

`images/template/avatar.svg` **同时还是浏览器标签页的图标（favicon）**，
所以它被保留下来继续使用。换头像时**不要删它**，否则标签页图标会 404。

想连 favicon 也换成自己的照片的话，告诉我一声。
