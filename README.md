[TOC]

# Rime-config

Rime 输入法配置

# 词库

- `wzyboy.dict.yaml` —— wzyboy 通过[点儿词库](http://gaokuan.ys168.com/)制作的词库
- `fcitx_wbx.dict.yaml` —— Fcitx 自带的五笔词库
- `zz.dict.yaml` —— 极点五笔 zz 快速输入词库
- `wubi86.dict.yaml` —— [rime-wubi 五筆字型](https://github.com/rime/rime-wubi)
- `weight0.dict.yaml` —— 五万生僻字词库

把相关文件全部放到 `/sdcard/rime` 目录下，重新部署。

最后对 `wubi86.schema.yaml` 打补丁：

```yaml
patch:
  translator/dictionary: fcitx_wbx.092m
```

# 生僻字专用字体

针对词库里的生僻字，Trime 还有个贴心的小设计：使用专门的字体来显示 CJK Ext-B 及之后的汉字。
做到 CJK Ext-B 至 CJK Ext-F 六万多个汉字全部收录的字体是[花园明朝](http://fonts.jp/hanazono/)（花園明朝）。

最后对 `trime.yaml` 打补丁：

```yaml
patch:
  "style/hanb_font": HanaMinB.ttf
```

# 参考

1. [RIME | 中州韻輸入法引擎](https://rime.im/)
2. [osfans/trime 同文输入法](https://github.com/osfans/trime)
3. [rime-wubi 五筆字型](https://github.com/rime/rime-wubi)
4. [rime/rime-pinyin-simp 袖珍简化字拼音](https://github.com/rime/rime-pinyin-simp)
5. [wzyboy《使用 Trime 在 Android 上输入五笔》](https://wzyboy.im/post/1251.html)
