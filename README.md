# Rime 配置文件

## 声明
基于原作者的融合拼音修改
融合了[【袖珍简化字拼音】](https://github.com/rime/rime-pinyin-simp/)、[【Rime 简体中文用户定制文件】](https://github.com/huaxianyan/Rime)和【Easy English】以实现中英文混合输入。   
Rime新手使用此方案，可以快速上手简体中文和常用英语的混合输入。
原作者GitHub仓库地址：https://github.com/tumuyan/rime-pinyin-simp


## 使用方法
* 目前本方案没有加入东风破，需要下载文件并放置到方案目录来使用。 
1. [下载文件](https://codeload.github.com/SaboZhang/RimeConfig/zip/main)、解压文件并复制到`Rime用户文件夹`内。GitHub下载慢可以使用[Gitee镜像下载](https://gitee.com/tao_SaboZhang/RimeConfig);用戶資料夾位置：  
    * 【中州韻】 ~/.config/ibus/rime/ （0.9.1 以下版本爲 ~/.ibus/rime/）
    * 【小狼毫】 %APPDATA%\Rime
    * 【鼠鬚管】 ~/Library/Rime/
2. 启用[袖珍简化字拼音]和［Easy English Nano]方案。
3. 打开 Rime 方案选单（输入状态下按Ctrl + ~），切换至「融合拼音」即可开始使用。

## 文件组成
* `pinyin_simp.dict.yaml` ：袖珍简化字拼音词库文件。此文件仅用于和原方案词库对比差异、保持同步，可直接删除
* `pinyin_simp.schema.yaml` ：袖珍简化字拼音方案文件。
- `pinyin_simp.custom.yaml` ：袖珍简化字拼音方案的客制化配置文件。
- `pinyin_simp.main.dict.yaml` ：词库中心文件。词库内容由 [袖珍简化字拼音](https://github.com/rime/rime-pinyin-simp) 默认词库pinyin_simp.dict.yaml修改而来，故合并两者并保持同步。
- `pinyin_simp_base.dict.yaml` ：基础词库，由额外词库文件引用使用，来源为项目 [https://github.com/alswl/Rime](https://github.com/alswl/Rime) 中的[「现代汉语常用词表」](https://raw.githubusercontent.com/alswl/Rime/master/luna_pinyin.xiandaihanyuchangyongcibiao.dict.yaml)。
- `cn_en.dict.yaml` ： 弃用，改为引用Easy English Nano方案输入英文。
- `zhwiki.dict.yaml` ：肥猫词库。来源为项目 [fcitx5-pinyin-zhwiki](https://github.com/felixonmars/fcitx5-pinyin-zhwiki)
以下词库仅保持结构，实际上并没用在维护：
- `pinyin_simp_custom.dict.yaml` ：自定义词语，由额外词库文件引用使用。如需添加自定义短语，建议编辑此文件。
- `pinyin_simp_pin.txt` ：候选固定，使用另一个翻译器并给极高权重来达到固定候选列表的目的，编辑时请记得给极高权重。

【Easy English Nano】
* `melt_eng.schema.yaml` 归属于【Easy English】，原作者是Patrick <ipatrickmac@gmail.com>，但是在Patrick的主页没有这个项目的仓库。
而github上[BlindingDark](https://github.com/BlindingDark/rime-easy-en)有在维护，使用了**LGPLv3**协议，但是与本方案分属不同分支。
* `melt_eng.dict.yaml` 英文主词库，作者tanzi，没有更多信息。在2016考研词汇大纲和六级单词的基础上进行修订。
* `melt_mult_language.dict.yaml`中英混合及其他语言的词库。目前词条数量为1019

【增补词库】  
求人不如求己，用[【深蓝词库转换】](https://github.com/studyzy/imewlconverter)转换搜狗细胞词库，并手动更新。（然而显而易见，搜狗目前的策略并不是通过更新离线词库来改善用户的输入体验）
- `pinyin_simp_chengyu.dict.yaml`：搜狗成语俗语细胞词库 https://pinyin.sogou.com/dict/detail/index/15097
- `pinyin_simp_gushi.dict.yaml`：搜狗古诗细胞词库 https://pinyin.sogou.com/dict/detail/index/2
- `luna_pinyin.emoji.cldr.dict.yaml`：Emoji表情词库 from https://github.com/jolicode/emoji-search
- `luna_pinyin.kaomoji.dict.yaml`：搜狗颜文字
- `luna_pinyin_simp.chaizi.dict.yaml`：搜狗U模式拆字字库
- `luna_pinyin.idiom.dict.yaml`：俗语、谚语词库
- `luna_pinyin.sougou.dict.yaml`：搜狗基础词库跟部分细胞词库的整合，包含我个人的搜狗同步的词库。

## 皮肤界面
直接上效果图吧
P 站风格
![image](https://github.com/SaboZhang/Picture/blob/master/QQ%E6%88%AA%E5%9B%BE20201025121514.png)

![image](https://github.com/SaboZhang/Picture/blob/master/QQ%E6%88%AA%E5%9B%BE20201025121555.png)

Windows10风格 
![image](https://github.com/SaboZhang/Picture/blob/master/QQ%E6%88%AA%E5%9B%BE20201025125100.png)

皮肤可以在输入法设定中直接选用，也可以在`weasel.custom.yaml`文件中进行自定义修改自己喜欢的配色。

## 其他

官方文档参考地址：https://github.com/rime/home/wiki/UserGuide
输入法下载地址：https://rime.im/download/
<details>
<summary>以下内容来自袖珍简化字拼音的Readme</summary>

# 袖珍简化字拼音

配方： ℞ **pinyin-simp**

[Rime](https://rime.im) 袖珍简化字拼音輸入方案

## 安裝

[東風破](https://github.com/rime/plum) 安裝口令： `bash rime-install pinyin-simp`

授權條款：見 [LICENSE](LICENSE)
</details>
