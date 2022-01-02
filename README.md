hostname = greasyfork.org, openuserjs.org, trade-acs.m.taobao.com, *.*apps.com, bea.sportq.com, api.meiyan.com, *.gao1gps.cn, avoscloud.com, app.flashdown365.com, m.samh.xndm.tech, mob2015.kekenet.com, api.m.jd.com, ios.prod.ftl.netflix.com, vipapi.jxedt.com, api.interpreter.caiyunai.com, pocketlists.com, dida365.com, ticktick.com, book.haitunwallet.com, mubu.com, app.xunjiepdf.com, miaow.yiyongcad.com, api.lennou.com, api.gkocr.com, vira.llsapp.com, commerce-.*api.faceu.mobi, commerce-api.faceu.mobi, api.revenuecat.com, api.rr.tv, editorapi.115.com, api.lakecoloring.com, ctrl.playcvn.com, dict.eudic.net, m.client.10010.com, api.wakamoment.ga, *.bh3.com, api.diyidan.net, api.flexibits.com, api.jiaonizuocai.com, api.sololearn.com, tncj.hortorgames.com, bkcd.b-cdn.net, souhu.mett.me, ayk.tmdidi.com, m.pearkin.com, claritywallpaper.com, bookapi.ihuman.com, rest.zhibo.tv, note.youdao.com, billing.peakcloud.org, api.ithome.com, www.xmind.cn, *.arten.cn, api.weiqire.com, api.shimo.im, pay.wecut.com, *.videostarapp.com, app.api.versa-ai.com, *.bjxkhc.com, api.591master.com, jdytv.cn, user.shywck.com, *.xunjie*.com, api.psy-1.com, snailsleep.net, api.weibo.cn, mapi.weibo.com, *.uve.weibo.com, mp.weixin.qq.com,app.bilibili.com, api.zhihu.com, link.zhihu.com, aweme*.snssdk.com,*.xiao*.com,  *.xiaoxiao*.com, *.musical.ly, *.amemv.com, p.du.163.com, getuserinfo.321mh.com, getuserinfo-globalapi.zymk.cn, ios.fuliapps.com, vsco.co, api.vnision.com, *.my10api.com, sp.kaola.com, r.inews.qq.com, apple.fuliapps.com, newdrugs.dxy.cn, app101.avictown.cc, api.hlo.xyz, api.ijo.xyz, www.luqijianggushi.com, account.wps.*, u.kanghuayun.com, api.gyrosco.pe, api1.dobenge.cn, api.mvmtv.com, mitaoapp.yeduapp.com, origin-prod-phoenix.jibjab.com, www.3ivf.com, pay.guoing.com, api.termius.com, api.bjxkhc.com, viva.v21xy.com,api.gotokeep.com, ap*.intsig.net, mp.bybutter.com, api.vuevideo.net, api.picsart.c*, api.meiease.c*, splice.oracle.*.com, api.gamer.com.tw, ios.xiangjiaoapps.com, apple.xiangjiaoapps.com, *.lagoapps.com, api.gamer.com.tw, *.xiangxiangapps.com, avatar-nct.nixcdn.com, spclient.wg.spotify.com, oa.zalo.me, origin-prod-phoenix.jibjab.com, api.meiease.c*, api.unfold.app, viva-asia1.vvbrd.com, graph.nhaccuatui.com, api.memrise.com , api.sync.me, pool.elsanow.io, lambda.us-east-1.amazonaws.com, api.mondlylanguages.com, api.busuu.com, owa.videoshowiosglobalserver.com:0, accounts.elevateapp.net, purchases.ws.pho.to, api-intl.mr.meitu.com, bmall.camera360.com, api.tv.zing.vn, api.calm.com, www.calm.com, api.global.mp3.zing.vn, apimboom2.globaldelight.net, photos.adobe.io, license.pdfexpert.com, subs.platforms.team, apic.musixmatch.com, api.getmimo.com, api.revenuecat.com, engbright.com, api.lingokids.com, www.peacefulsoundsapp.com, duolingo-leaderboards-prod.duolingo.com, mobile-api.adguard.com, api.blinkist.com, api-kinemaster-assetstore.*, api.pushover.net, ap*.intsig.net, api.overhq.com, receipt-validator.herewetest.com, lcs-mobile-cops.adobe.io, education.github.com, backend.getdrafts.com, ssl-api.itranslateapp.com, sk.ulysses.app, dayone.me, license.enpass.io, mp.bybutter.com, *.grammarly.com, splice.oracle.*.com, api.keepkeep.com, planner5d.com, secure.istreamer.com, www.api.monkeyuni.net, api.textnow.me

# Chavy box (多账号Cookie保存切换)
# 访问:  http://boxjs.com 管理
^https?://boxjs.com/api url script-request-body https://gitee.com/chavyleung/scripts/raw/master/chavy.box.js
^https?://boxjs.com(/home|/sub|/my|/app|/log|/revert)?($|\/) url script-echo-response https://gitee.com/chavyleung/scripts/raw/master/chavy.box.js

##NobyDa

# 去微博应用内广告 (By yichahucha)
^https?://(sdk|wb)app.uve.weibo.com(/interface/sdk/sdkad.php|/wbapplua/wbpullad.lua) url script-response-body https://raw.githubusercontent.com/yichahucha/surge/master/wb_launch.js
^https?://m?api\.weibo\.c(n|om)/2/(statuses/(unread|extend|positives/get|(friends|video)(/|_)(mix)?timeline)|stories/(video_stream|home_list)|(groups|fangle)/timeline|profile/statuses|comments/build_comments|photo/recommend_list|service/picfeed|searchall|cardlist|page|!/photos/pic_recommend_status|video/tiny_stream_video_list|photo/info) url script-response-body https://raw.githubusercontent.com/yichahucha/surge/master/wb_ad.js

# 去微信公众号广告 (By Choler)
^https?:\/\/mp\.weixin\.qq\.com\/mp\/getappmsgad url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/File/Wechat.js

# 知乎去广告 (By onewayticket255)
https://api.zhihu.com/(ad|drama|fringe|commercial|market/popover|search/(top|preset|tab)|.*featured-comment-ad) url reject-200
https://api.zhihu.com/people/ url script-response-body https://raw.githubusercontent.com/onewayticket255/Surge-Script/master/surge%20zhihu%20people.js
https://api.zhihu.com/moments/recommend url script-response-body https://raw.githubusercontent.com/onewayticket255/Surge-Script/master/surge%20zhihu%20feed.js
https://api.zhihu.com/topstory/recommend url script-response-body https://raw.githubusercontent.com/onewayticket255/Surge-Script/master/surge%20zhihu%20recommend.js
https://api.zhihu.com/v4/questions url script-response-body https://raw.githubusercontent.com/onewayticket255/Surge-Script/master/surge%20zhihu%20answer.js
https?://link.zhihu.com/?target= url script-request-header https://raw.githubusercontent.com/onewayticket255/Surge-Script/master/surge%20zhihu%20link.js

# 哔哩哔哩动画去广告 (By onewayticket255)
https://app.bilibili.com/x/v2/(splash|search/(defaultword|square)) url reject-200
https://api.bilibili.com/x/v2/dm/ad url reject-200
#https://app.bilibili.com/x/v2/space\?access_key url script-response-body https://raw.githubusercontent.com/onewayticket255/Surge-Script/master/surge%20bilibili%20space.js
https://app.bilibili.com/x/resource/show/tab\?access_key url script-response-body https://raw.githubusercontent.com/onewayticket255/Surge-Script/master/surge%20bilibili%20tab.js
https://app.bilibili.com/x/v2/feed/index\?access_key url script-response-body https://raw.githubusercontent.com/onewayticket255/Surge-Script/master/surge%20bilibili%20feed.js
https://app.bilibili.com/x/v2/view\?access_key url script-response-body https://raw.githubusercontent.com/onewayticket255/Surge-Script/master/surge%20bilibili%20view%20relate.js
https://api.bilibili.com/x/v2/reply/main\?access_key url script-response-body https://raw.githubusercontent.com/onewayticket255/Surge-Script/master/surge%20bilibili%20reply.js
https://api.live.bilibili.com/xlive/app-room/v1/index/getInfoByRoom\?access_key url script-response-body https://raw.githubusercontent.com/onewayticket255/Surge-Script/master/surge%20bilibili%20live.js


# 小小影视会员
https:\/\/.*.xiao*(img|apps|appxs).com url request-header (\r\n)Cookie:.+(\r\n) request-header $1Cookie: xxx_api_auth=6131333537653261363463323331666265663763396239663835636662373930$2

# 爱美剧Vip (by huihui）(官网：app.meiju2018.com)
#ads
^http(s)://api.bjxkhc.com/index.php/app/ios/ads/index url reject-dict
^http(s)://api.bjxkhc.com/index.php/app/ios/ver/index_ios$ url reject
^http(s)://api.bjxkhc.com/index.php/app/ios/pay/ok$ url reject-dict
#VIP&ads
^http(s)://api.bjxkhc.com/index.php/app/ios/(vod/show|(user|vod|topic|type)/index) url script-response-body https://raw.githubusercontent.com/wf021325/qx/master/js/aimeiju.js

# 网易蜗牛读书VIP (By yxiaocai and JO2EY)
^https?://p\.du\.163\.com/readtime/info.json url reject
^https?:\/\/p\.du\.163\.com\/gain\/readtime\/info\.json url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/File/wnyd.js

# 知音漫客VIP (By mieqq)
^https://getuserinfo-globalapi.zymk.cn/app_api/v5/(getuserinfo|coin_account|getuserinfo_ticket|getcomicinfo)/ url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/File/Zymh.js

# 滴答清单 pro
^https:\/\/(ticktick|dida365)\.com\/api\/v2\/user\/status url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/NobyDa/QuantumultX/File/DiDaQingDan.js

# VSCO滤镜VIP
^https?:\/\/vsco\.co\/api\/subscriptions\/2.1\/user-subscriptions\/ url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/File/vsco.js

# 大片-视频编辑器 VIP
^https?:\/\/api\.vnision\.com\/v1\/(users\/|banners) url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/File/dapian.js

# 香蕉视频
# VIP (By Gx3dong)
https:\/\/.*\.*apps.com url request-header Cookie:.+ request-header Cookie: xxx_api_auth=3433346533343130636136363935363132383864623761323737363464376233


# 陆琪讲故事
^https:\/\/www\.luqijianggushi\.com\/api\/v2\/user\/get url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/luqi.js

# Gyroscope 解锁 pro (By Maasea)
^https:\/\/api\.gyrosco\.pe\/v1\/account\/$ url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/NobyDa/Surge/JS/gyroscope.js


# JibJab解锁pro
^https:\/\/origin-prod-phoenix\.jibjab\.com\/v1\/user url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/jibjab.js

# Termius 解锁本地pro  (By Maasea)
https:\/\/api\.termius\.com\/api\/v3\/bulk\/account\/ url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/NobyDa/Surge/JS/Termius.js

# 小影 解锁Vip (By @hiepkimcdtk55)
^https:\/\/viva\.v21xy\.com\/api\/rest\/u\/vip url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/vivavideo.js

# VUE pro
^https:\/\/api\.vuevideo\.net\/api\/v1\/(users\/.+\/profile|subtitle\/prepare) url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/VUE.js

# NiChi 解锁素材
^https?:\/\/mp\.bybutter\.com\/mood\/(official-templates|privileges) url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/NiChi.js

# PicsArt美易 pro
^https:\/\/api\.(picsart|meiease)\.c(n|om)\/users\/show\/me\.json url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/PicsArt.js

# Splice 视频编辑器 pro
^https:\/\/splice\.oracle\.\w+\.com\/devices\/me url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/NobyDa/Surge/JS/Splice.js


#皮皮虾 去广告去水印
^https?://.*\.snssdk\.com/bds/(feed/stream|comment/cell_reply|cell/cell_comment|cell/detail|ward/list|user/favorite|user/cell_coment|user/cell_userfeed|user/publish_list) url script-response-body https://raw.githubusercontent.com/Liquor030/Sub_Ruleset/master/Script/Super.js

##大雄脚本组

# 驾校一点通 (by @superuv)
^https:\/\/vipapi\.jxedt\.com\/vip\/check url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/jxydt.js

# 彩云小译   (by @superuv)
^https:\/\/api\.interpreter\.caiyunai\.com\/v1\/user url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/cyxy.js

#Bear熊掌记  内购解锁
^https:\/\/buy\.itunes\.apple\.com\/verifyReceipt url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/bear.js

#Pocket list (by @superuv)
^https:\/\/pocketlists\.com\/api\/v1\/pocketlists.me.get url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/pock.js

#海豚记账 (by @superuv)
https:\/\/book\.haitunwallet\.com\/app\/vip\/status url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/HTJZ.js

#幕布 (by @superuv)
https:\/\/mubu\.com\/api\/app\/user\/info url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/mb.js

#智能证件照相机 (by @superuv)
^https:\/\/app\.xunjiepdf\.com\/api\/v4\/virtualactregister url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/znzj.js

#猫咪翻译(by @superuv)
http:\/\/miaow\.yiyongcad\.com\/api\/v4\/memprofile url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/mmfy.js

#微商助手(by @superuv)
https:\/\/api\.lennou\.com\/user\/info url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/wszs.js

#gk扫描仪(by @superuv)
^https:\/\/api\.gkocr\.com\/api\/userlogin1.php url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/smy.js

#流利说.阅读 (by@火羽&@singee)
^https?:\/\/vira\.llsapp\.com\/api\/v2\/readings\/(accessible|limitation) url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/llyd.js

#人人视频 (by@george Jiang & R)
^https:\/\/api\.rr\.tv(\/user\/privilege\/list|\/ad\/getAll|\/rrtv-video\/v4plus\/season\/detail) url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/rrtv.js

#abaenglish (未测试)
^https:\/\/api\.revenuecat\.com\/v1\/(receipts|\d{1,})$ url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/abaenglish.vip.js

#轻颜相机 & ulike & 蒸汽波相机(vaporcam)三合一 解锁VIP(By @s y & Alex0510)
https://(commerce-.*api|pay).(faceu|wecut).(com|mobi)/(commerce|apple)/(iosAppVerifyReceipt.php|v1/subscription/user_info) url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/qyxj.js

# 115离线 (请仔细阅读脚本内使用说明 By ikanam)
^https:\/\/editorapi\.115\.com.* url 302 http://115.com/lx?taskdg=1
^http:\/\/115\.com\/lx.*$ url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/115lx.js

#lake
^https:\/\/api\.lakecoloring\.com\/v1\/receipt url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/lake.js

#人人影视字幕组(商店版)去广告,保留轮播推荐影片(By @Kaya)
^http://ctrl.playcvn.com/app/(init|ads) url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/YYeTs.js

#每日英语阅读/每日外刊 解锁课程  (By chamberlen)
^https:\/\/dict\.eudic\.net\/jingting\/GetThisChapterTaskStatus? url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/mryy.js

#联通营业厅 去轮播广告 (By Wangsc1)
^https?://m.client.10010.com/uniAdmsInterface/getHomePageAd url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/china_unicom.js


#第一弹 去广告+原画 (By Miao Miao)
^https:\/\/api\.diyidan\.net\/v0\.3\/(user\/personal_homepage|vip_user\/info|tv_series\/index\?appChanne) url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/Diyidan.js
# 修复下载视频清晰度
(http://musicapi\.diyidan\.net/tv_series/video/download/\d+)/(1|2) url 302 $1/4

#Fantastical 内购解锁 (By @sunshy)
^https:\/\/api\.flexibits\.com\/v1\/(auth|account)\/(device|details|appstore-receipt)\/$ url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/fantastical.js

#菜谱大全解锁vip (By @photonmang)
https?:\/\/api\.jiaonizuocai\.com url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/cpdq.js

#SoloLearn Unlock PRO & Platinum Moderator (By @sunshy)
https:\/\/api\.sololearn\.com\/(authenticateDevice|challenge\/GetContestFeed|Profile\/GetProfile)$ url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/sololearn.js

#头脑吃鸡
^https://tncj.hortorgames.com/chicken/fight/(answer|findQuiz) url script-response-body https://raw.githubusercontent.com/chavyleung/scripts/master/tncj/tncj.min.js

#Pear 雪梨
^https:\/\/(www\.baidu.com2\.club|ayk\.tmdidi\.com|m\.pearkin\.com|souhu\.mett\.me|bkcd\.b-cdn\.net)\/(api\/movie\/WatchMovie|api\/Account\/CheckVip|api\/account\/IndexDetail) url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/pear.js

#克拉壁纸  解锁付费壁纸 (By @Dachaw)
^https:\/\/claritywallpaper\.com\/clarity\/api\/(userInfo|special\/queryByCatalogAll) url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/clarity.js

#洪恩双语绘本 (By 军哥哥)
https:\/\/bookapi\.ihuman\.com\/(v1\/get\_user\_info|v1\/get\_purchase\_list) url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/hnsyhb.js

#中国体育直播unlock (By 军哥哥)
http:\/\/rest\.zhibo\.tv\/room\/get\-room\-info\-v430 url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/zgtyzb.js

# 有道云笔记VIP (ByAlex0510)
https://note.youdao.com/yws/(mapi/payment|api/self) url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/ydybj.js

#Peak 解锁Pro
^https:\/\/billing\.peakcloud\.org\/billing\/2\/user\/me? url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/peak.js

# IT之家 去新闻列表广告
^https?:\/\/api\.ithome\.com\/json\/slide\/index url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/ITHome.js
^https?:\/\/api\.ithome\.com\/json\/(newslist|listpage)\/news url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/ITHome.js

# XMind思维导图 (by @JigsaWo)
https:\/\/www\.xmind\.cn\/\_res\/devices url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/XMind.js

# 万里影视 （by LTribe）
^http?:\/\/.*\.arten.cn/login/login url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/Wanliyingshi.js

# 奇热小说 解锁收费章节(By @@ios4521)
^https://api.weiqire.com/api3/(visitor/|user/unlockCharpter) url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/qrxs.js

# 石墨文档 (By Alex0510)
https://api.shimo.im/users/ url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/shimo.js

#VideoStar Unlock（by LTribe）
^https?:\/\/.*\.videostarapp\.com\/scripts\/subsNew\.php url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/VideoStar.js

# Pillow (By @CheeryTodo)
https:\/\/api\.revenuecat\.com\/v1\/(subscribers|receipts) url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/pillow.js

# 马卡龙 (By @CheeryTodo)
https://app.api.versa-ai.com/pay/order/iap/check url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/mkl.js

# 韩剧TV (By 凉意)
# 下载地址请看脚本内说明
^https\:\/\/hjapi\.bjxkhc\.com\/v2d2\/users\/.*\/member url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/hanjuTV.js

# 手机硬件管家 (By Alex0510)
http:\/\/api\.591master\.com\:8081\/(1.0|3.6.8)\/ui(forum|common)\/(downloadwallpaper|getuser) url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/sjyjgj.js

# 筋斗云tv (By 凉意)
^http\:\/\/jdytv\.cn\/login\/login\/veifys url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/jdyTV.js

# 花椒视频 (By Alex0510)
http://user.shywck.com/user/userinfo url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/hjsp.js

# 迅捷应用6合1 （by LTribe）
^https?:\/\/.*\.xunjie.*\.com\/api\/v\d\/* url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/xunjie.js

# 小睡眠（by 黑黑酱）
^https:\/\/api\.psy-1\.com\/cosleep\/user\/info url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/xiaoshuimian.js

#蜗牛睡眠会员（by黑黑酱）
^https:\/\/snailsleep\.net\/snail\/v1\/profile\/get url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/wnsm.js

# 可可英语会员
^https:\/\/mob2015\.kekenet\.com\/keke\/mobile\/index\.php url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/kkyy.js

# 飒漫画 (By @u18888)
^https:\/\/m\.samh\.xndm\.tech\/userapi\/info\/v1\/getuserinfo url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/Smh.js

# 闪电下载vip (By 凉意)
^http\:\/\/app\.flashdown365\.com\/ios\/login url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/sdxz.js

# 西窗烛 （By 黑黑酱）
^https:\/\/avoscloud\.com\/1\.1\/users\/ url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/xcz.js

# JAV101无限观看 (By 凉意)
^https\:\/\/pwaapi\.gao1gps\.cn\/v1\/user\/info url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/JAV101.js

# 美颜相机一次性解锁内购（by黑黑酱）
^https:\/\/api\.meiyan\.com\/iap\/verify\.json url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/myxj.js

# Fit健身会员 （by黑黑酱）
^https:\/\/bea\.sportq\.com\/SFitWeb\/sfit\/getUserBaseInfo url script-response-body https://raw.githubusercontent.com/nzw9314/QuantumultX/master/Script/fit.js

# 油猴转换器 (by Peng-YM)
https:\/\/greasyfork\.org\/scripts\/.*\.user\.js url script-response-body https://raw.githubusercontent.com/Peng-YM/QuanX/master/Rewrites/GreasyFork/greasy-fork.js

