# 《皮毛之下》

## 作者的话

这是作者的第二本书。第一本写崩了，才三章就崩了。所以也还算是新人作者。不太会写，没什么灵感，写的不太好，还望轻喷。

## 关于格式和……Git？

小说主题使用的 Markdown 格式，因为可以使用 XAML 来加上元信息（标题和日期）而且……好吧，就等有心人发现些什么东西了。

至于为什么用 Git？那是因为……我可以多分支并行写好几个支线（好吧，是纯闲的。）

其实最开始突然想到加 Git 确实是因为这个原因，到后来我发现我他妈根本不知道怎么写支线，他妈的我写单线我都给自己写的 CPU 差点烧融。（还想写支线，哎，走都没学会，你他妈倒学起跑来了）

但是后来，我有的时候会手机写，有的时候会电脑写。我经常要在手机和电脑之间同步内容，同时也是因为我是一个业余程序员的原因，我突然想到，Git 好像也是个不错的小玩意，就用着了。

## 关于发布

你们除了可以在 [GitHub](https://www.github.com/cnbilinyj/BeneathTheFurries) 里面读这本小说，  
还可以在我的[个人网站](https://looseice-furry-vcard.ggff.net/novels/cf6fe50f-b414-47a3-9ec7-513944a6d31b/)里面读这本小说。

## 关于 AI 文

在 GitHub 里面可以看到我的所有保存记录。理论上说，每次小修改，只要我在手机上有保存，就会产生一次提交。

    auto_commit() {
      if [[ $(git --no-pager log -1 --format=%s | awk '{printf $2}') == $(date +%Y-%m-%d) ]]; then
        local new_num=$(git --no-pager log -1 --format=%s | awk '{print $3}' | jq -Rr 'split("#")[1] | tonumber + 1 | "#" + tostring')
      else
        local new_num='#1'
      fi
      local new_msg="编辑 $(date +%Y-%m-%d) $new_num $(date +%H:%M)"
      git add -A && git commit -m "$new_msg" && git push origin writer
    }
    
    

总之，这是我写的，不是 AI 写的。

<!-- AI 确实太好用了，因为它真的能把你干红温。我只有极少数地方遣词造句我可能会用到 AI。

如果文章主体用 AI 的话，是真的会把你气死的。因为它会在各种地方违背你的初始设定，或者违背它刚写过的东西。是的，就上一句它刚写过，下一句都会和上一句产生矛盾。

只能说不愧是 AI，人工白痴嘛，（Artifical Idiot，人工白痴）

所以我是绝对不可能在文章主体里面使用AI的，我已经红温不下……我也说不清多少次了，反正绝对不下50次。 -->