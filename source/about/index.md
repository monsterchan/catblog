---
title: about me
date: 2018-12-12 22:14:36
keywords: 关于
description: 期待您走进我的世界里，一起追寻更好的自己！
comments: false
photos: https://cdn.jsdelivr.net/gh/monsterchan/cdn@1.6/img/banner/about.jpg
---
{% raw %}
<div class="moe-mashiro" style="text-align:center; font-size: 50px; margin-bottom: 20px;">[沐猫と陈]</div>
<div id="hello-mashiro" class="popcontainer" style="min-height: 300px; padding: 2px 6px 4px; background-color: rgba(242, 242, 242, 0.5); border-radius: 10px;">
  <center>
  <p>
  </p>
  <h4>
  与<ruby>
  陈<rp>
  （</rp>
  <rt>
  世界太大，大的人海茫茫，世界太小，小的恰使我们相遇！</rt>
  <rp>
  ）</rp>
  </ruby>
  对话中...</h4>
  <p>
  </p>
  </center>
  <bot-ui></botui>
</div>
<script src="https://cdn.jsdelivr.net/vue/latest/vue.min.js"></script>
<script src="https://unpkg.com/botui/build/botui.min.js"></script>
<script>
function bot_ui_ini() {
    var botui = new BotUI("hello-mashiro");
    botui.message.add({
        delay: 800,
        content: "Hi, Welcome you come into my life!👋"
    }).then(function () {
        botui.message.add({
            delay: 1100,
            content: "我是 陈"
        }).then(function () {
            botui.message.add({
                delay: 1100,
                content: "一个萌萌的蓝孩子~"
            }).then(function () {
                botui.action.button({
                    delay: 1600,
                    action: [{
                        text: "然后呢？ 😃",
                        value: "sure"
                    }, {
                        text: "少废话！ 🙄",
                        value: "skip"
                    }]
                }).then(function (a) {
                    "sure" == a.value && sure();
                    "skip" == a.value && end()
                })
            })
        })
    });
    var sure = function () {
            botui.message.add({
                delay: 600,
                content: "😘"
            }).then(function () {
                secondpart()
            })
        },
        end = function () {
            botui.message.add({
                delay: 600,
                content: "![qieman.jpg](https://i.loli.net/2020/01/11/dEGZwQtXrMykCFq.jpg)"
            })
        },
        secondpart = function () {
            botui.message.add({
                delay: 1500,
                content: "目前就读于家里蹲学"
            }).then(function () {
                botui.message.add({
                    delay: 1500,
                    content: "向往技术却技术烂…"
                }).then(function () {
                    botui.message.add({
                        delay: 1200,
                        content: "因为数据分析也需要Coder嘛"
                    }).then(function () {
                        botui.message.add({
                            delay: 1500,
                            content: "主攻 Java语言和 Python，略懂 Vue，偶尔也折腾 HTML/CSS/JavaScript"
                        }).then(function () {
                            botui.message.add({
                                delay: 1500,
                                content: "研究的方向，是数据分析（data science）以及机器学习（machine learning）和人工智能"
                            }).then(function () {
                                botui.message.add({
                                    delay: 1800,
                                    content: "喜欢画画，希望有一天能够被称为画师"
                                }).then(function () {
                                    botui.action.button({
                                        delay: 1100,
                                        action: [{
                                            text: "为什么叫陈呢？ 🤔",
                                            value: "why-name"
                                        }]
                                    }).then(function (a) {
                                        thirdpart()
                                    })
                                })
                            })
                        })
                    })
                })
            })
        },
        thirdpart = function () {
            botui.message.add({
                delay: 1E3,
                content: "陈以及站名都来自臆想，因为和主角有一样的爱好~ 如果有兴趣可以找找首页上的视频~"
            }).then(function () {
                botui.action.button({
                    delay: 1500,
                    action: [{
                        text: "为什么是沐猫呢？ 🤔",
                        value: "why-cat"
                    }]
                }).then(function (a) {
                    fourthpart()
                })
            })
        },
        fourthpart = function () {
            botui.message.add({
                delay: 1E3,
                content: "因为对GitHub有种执念… "
            }).then(function () {
                botui.message.add({
                    delay: 1100,
                    content: "而且我真的是猫控！"
                }).then(function () {
                    botui.action.button({
                        delay: 1500,
                        action: [{
                            text: "域名有什么含意吗？(ง •_•)ง",
                            value: "why-domain"
                        }]
                    }).then(function (a) {
                        fifthpart()
                    })
                })
            })
        },
        fifthpart = function () {
            botui.message.add({
                delay: 1E3,
                content: "emmmm，That is my full name!"
            }).then(function () {
                botui.message.add({
                    delay: 1600,
                    content: "那么，看看我的博客吧，别忘了留言哟！ ^_^"
                })
            })
        } 
}
bot_ui_ini()
</script>
{% endraw %}