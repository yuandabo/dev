\\172.16.4.192\it_software
\\172.16.10.4\共享测试包\袁波分支-秦丝进销存

qinsiyb

xiaolintest
xiaolin123

lilaobantest
lilaoban123

xiaojiuzitest
xiaojiuzi123

进销存
免费版账号：
17771779999  hh123456
16638939915  czq12345633

15369462534
Qinsi1234.

17608484272
a123456

13686446394
a123456

18002120013 gwy123456789

15970796406
hh123456

18270777302
qzl123456

17700000003 123456aa

生意通

17608484272 a123456 
17608484273 a123456

vip 吊牌 打包测试
启动页上传打包测试
```js
下载图片: pictureModalDownload

货号\名称\条码

显示点击的商品图片 showGoodImage

$scope.showGoodImage = function (url) 

图片分享图篇 shareGoodsImgs => shareImgsFun => getCompressPicture

获取图片后缀方法： getAlbummType

// 判断下载图片的质量
            $rootScope.downPictureQuality

// 查看原图时取图片路径
            $rootScope.getWaterMarkPhoto = function (url) {
//显示点击的图片
            $scope.showGoodImage = function () {

//show - 图片详情窗口
            $scope.showTmsShopPhotoAlbumGalleryPictureModal = function (list, index) {

选择商品图片到一个数组中
        var selectGoodsImgsToArray

//show - 图片详情窗口
            $scope.showTmsShopPhotoAlbumGalleryPictureModal

getCompressPicture 

```


```js
// 多图分享
            $scope.wechatShareImgs
socialsharing

保存 : cordova.plugins.saveImageToAlbum.save
         	

动态保存 $rootScope.saveImageToAlbum([img]);


本周主要开发任务是进销存vip增值服务版本计划。随着开发的进行，对进销存代码有了更深的理解，与同事之间也熟悉了起来，开发顺利，联调顺利，计划下周完成测试并上线。

vip 版本:



秦丝零售版： 
参考页面： accountInfo
会员营销： memberMark


秦丝生意通：
会员改版待迁移界面：good/scan.html  
水印核心方法： getWaterMarkPhoto()

已处理的图片水印：
图片详情显示、分享，涉及方法： getcompresspictrue
商品详情分享 getcompresspictrue,
图片详情保存 saveImage -> cordova.plugins.saveImageToAlbum.save
商品列表分享 getcompresspictrue,
商品新增 getAlbummType
商品管理列表分享 getcompresspictrue,
商品图片大图预览： showTmsShopPhotoAlbumGalleryPictureModal

‘销售单/销售退货单/采购单/采购退货单/盘点单/库存调拨单 查看原图 
```
vip 报表功能：原生表格

```js
10.11: 解决bug dev-

bubble 逻辑： 
/**
             * @description: 水印新功能提示气泡
             */            
            if (!$window.localStorage['waterMarkBubbleShow' + $scope.mainUserConfig.userId]) {
                $scope.waterMarkBubbleShow = true;
            } else {
                $scope.waterMarkBubbleShow = false;
            }

            $scope.closeBubbleTips = function(right){
                $window.localStorage['waterMarkBubbleShow' + $scope.mainUserConfig.userId] = 1;
                $scope.waterMarkBubbleShow = false;
            }


// 标签选择框
            $scope.openLabelMenuPopover = function ($event) {
                $scope.setAliLog($state.current.name, "good_openLabelMenuPopover");
                if ($scope.labelMenuPopover) {
                    $scope.labelMenuPopover.show($event);
                } else {
                    $ionicPopover.fromTemplateUrl('labelMenuPopover.html', {
                        scope: $scope
                    }).then(function (popover) {
                        $scope.labelMenuPopover = popover;
                        $scope.labelMenuPopover.show($event);
                    });
                }
            };


炙热销 unmarketableOrHotGoodsCtrl

/**
 * @description: 
 * @param {type} 
 * @return: 
 */


// 表格组件

// fixed
<div class="lb-reportTotal-table-fixed" ng-if="currentViewType === 'table'">
        <table class="lb-table lb-reportTotal-table" style="min-width: 800px;position: relative;z-index: 5;">
            <thead>
                <tr>
                    <th class="lb-table__cell" ng-repeat="head in tableHeadList" colspan="1" rowspan="1">
                        <span class="lb-table_cell-span"
                            ng-style="{ 'width': head.width ? head.width : '100px' }"
                            ng-click="tableHeadSpanClickHandle($event, $index)">
                            <span>{{head.label}}</span>
                            <span ng-if="$index === 0" data-iconType="dropdowmicon" class="lb-reportTotal-table-dropdownicon">
                                <i data-iconType="dropdowmicon" class="icon ion-arrow-down-b"
                                    ng-class="{ 'ion-arrow-right-b': dropdownActive }"
                                    ng-style="{ 'color' : dropdownSortAciton ? '#00a3f0' : '' }"></i>
                            </span>
                            <span ng-if="$index !== 0" data-iconType="sortIcon" class="lb-reportTotal-table-sortIcon">
                                <i class="icon ion-arrow-up-b" data-iconType="sortIcon" style="top: -4px;"
                                    ng-style="getColomnSortStyle('asc',$index)"></i>
                                <i class="icon ion-arrow-down-b" data-iconType="sortIcon" style="top: 2px"
                                    ng-style="getColomnSortStyle('desc',$index)"></i>
                            </span>
                        </span>
                    </th>
                </tr>
            </thead>
        </table>
        <table class="lb-table lb-reportTotal-table lb-reportTotal-table-body" id="lb-reportTotal-table-fixed-tbody" style="min-width: 800px;">
            <tbody>
                <tr ng-repeat="head in tableDataList" ng-init="outerIndex=$index" class="lb-table__row">
                    <td ng-repeat="head in tableHeadList" class="lb-table__cell" rowspan="1" colspan="1">
                        <span class="lb-table_cell-span" ng-style="{ 'width': head.width ? head.width : '100px' }">{{tableDataList[outerIndex][head.value] || 0}}</span>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>


// <div class="lb-goodsSummartReport-content-warp" ng-if="currentViewType === 'table'">
            <div class="lb-reportTotal-table-warp">
                <div class="lb-reportTotal-table lb-reportTotal-table-thead">
                    <ion-scroll class="lb-reportTable-head-scoll" id="reportTableHead" direction="x"
                        ignoreScrollStart="true" on-scroll="reportTableScrollHandle()">
                        <table class="lb-table" style="min-width: 800px;">
                            <thead>
                                <tr>
                                    <th class="lb-table__cell" ng-repeat="head in tableHeadList" colspan="1" rowspan="1">
                                        <span class="lb-reportTotal-table-headspan lb-table_cell-span"
                                            ng-style="{ 'width': head.width ? head.width : '100px' }"
                                            ng-click="tableHeadSpanClickHandle($event, $index, head)">
                                            <span class="lb-reportTotal-table-headspan-label">{{head.label}}</span>
                                            <span ng-if="$index === 0" data-iconType="dropdowmicon"
                                                class="lb-reportTotal-table-dropdownicon">
                                                <i data-iconType="dropdowmicon" class="icon ion-arrow-down-b"
                                                    ng-class="{ 'ion-arrow-right-b': dropdownActive }"
                                                    ng-style="{ 'color' : dropdownSortAciton ? '#00a3f0' : '' }"></i>
                                            </span>
                                            <span ng-if="$index !== 0" data-iconType="sortIcon"
                                                class="lb-reportTotal-table-sortIcon">
                                                <i class="icon ion-arrow-up-b" data-iconType="sortIcon" style="top: -4px;"
                                                    ng-style="getColomnSortStyle('asc',$index)"></i>
                                                <i class="icon ion-arrow-down-b" data-iconType="sortIcon" style="top: 2px"
                                                    ng-style="getColomnSortStyle('desc',$index)"></i>
                                            </span>
                                        </span>
                                    </th>
                                </tr>
                            </thead>
                        </table>
                    </ion-scroll>
                </div>
                <div class="lb-reportTotal-table lb-reportTotal-table-body">
                    <ion-scroll style="height: 100%;" id="reportTableBody" direction="xy" ignoreScrollStart="true"
                        on-scroll="tableBodyScrollHandle($event)">
                        <table class="lb-table" style="min-width: 800px;">
                            <tbody>
                                <tr ng-repeat="head in tableDataList" ng-init="outerIndex=$index" class="lb-table__row">
                                    <td ng-repeat="head in tableHeadList" class="lb-table__cell" rowspan="1" colspan="1">
                                        <span class="lb-table_cell-span" ng-style="{ 'width': head.width ? head.width : '100px' }">{{tableDataList[outerIndex][head.value]  || 0}}</span>
                                    </td>
                                </tr>
                                <tr>
                                    <td class="pr">
                                        <span>
                                            <ion-infinite-scroll on-infinite="getMore();" ng-if="loadMoreBtn" distance="1%" style="position: absolute;top: 0;left: 0;width: 100vw;"></ion-infinite-scroll>
                                        </span>
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                    </ion-scroll>
                </div>
            </div>
        </div>


//  保持 thread 和 tbody x 轴滑动一致 并设置 Boxshadow
            // var shadowStyleStr = '0 0 10px rgb(0 0 0 / 12%)'
            var reportTableHead = document.querySelector('#reportTableHead')
            var reportTableBody = document.querySelector('#reportTableBody')
            // var tableFixed = document.querySelector('.lb-reportTotal-table-fixed')
            // var tableFixedTbody = document.querySelector('#lb-reportTotal-table-fixed-tbody')
            // var tableFixedHead = document.querySelector('.lb-reportTotal-table-fixedHead')
            var CLIENTWIDTH = document.body.clientWidth;
            var MAXTRANSITONX
            $scope.tableBodyScrollHandle = function () {
                if (!reportTableBody) reportTableBody = document.querySelector('#reportTableBody')  // 节约性能
                // if (!tableFixed) tableFixed = document.querySelector('.lb-reportTotal-table-fixed')
                if (!reportTableHead) reportTableHead = document.querySelector('#reportTableHead')
                if (!MAXTRANSITONX) MAXTRANSITONX = (reportTableBody.querySelector('tbody').clientWidth - CLIENTWIDTH) * 0.91
                // if (!tableFixedTbody) tableFixedTbody = document.querySelector('#lb-reportTotal-table-fixed-tbody')
                // if (!tableFixedHead) tableFixedHead = document.querySelector('.lb-reportTotal-table-fixedHead')
               
                var str = reportTableBody.querySelector('.scroll').style.transform;

                var index = str.indexOf(',')
                var translateX = str.slice(12 , index)
                var translateXNumber = parseInt(translateX)

                // var translateY = str.slice(index + 1 , str.indexOf(',', index + 1)).trim()

                if (translateXNumber <= MAXTRANSITONX) {
                    $scope.isYHandle = false
                } else {
                    $scope.isYHandle = true
                }
                // if (translateX === '0px'){  // 在最左边
                //     tableFixed.style.boxShadow = '';
                //     tableFixed.style.visibility = 'hidden'
                // } else {
                //     tableFixed.style.boxShadow = shadowStyleStr
                //     tableFixed.style.visibility = 'visible'
                // }

                reportTableHead.querySelector('.scroll').style.transform = "translate3d(" + translateX + ", 0px, 0px) scale(1)"

                // tableFixedTbody.style.transform = "translate3d(0px, " + translateY + ", 0px) scale(1)"
            }


 $scope.reportTableScrollHandle = function () {
                if (!reportTableHead) reportTableHead = document.querySelector('#reportTableHead')  // 节约性能
                // if (!tableFixed) tableFixed = document.querySelector('.lb-reportTotal-table-fixed')
                if (!reportTableBody) reportTableBody = document.querySelector('#reportTableBody')
                // if (!tableFixedHead) tableFixedHead = document.querySelector('.lb-reportTotal-table-fixedHead')
                var str = reportTableHead.querySelector('.scroll').style.transform;
                // var tableFixed = document.querySelector('.lb-reportTotal-table-fixed') || {}
                // if (str.indexOf('translate3d(0px, 0px, 0px)') !== -1){  // 在最左边
                //     tableFixed.style.boxShadow = '';
                // } else {
                //     tableFixed.style.boxShadow = shadowStyleStr
                // }
                reportTableBody.querySelector('.scroll').style.transform = str
                // tableFixedHead.querySelector('.scroll').style.transform = str
            }

// var reportContentScroll = document.querySelector('#reportContentScroll')

            // angular.element(document.querySelector('#reportContentScroll')).bind('scroll', function($event){
            //     $event.stopPropagation()
            //     // $event.stopImmediatePropagation()
            // })


            // angular.element(document.querySelector('#reportTableBody')).bind('scroll', function($event){
            //     $event.stopPropagation()
            //     // $event.stopImmediatePropagation()
            // })

```
# 表格组件：
- 描述: 在通过transform虚拟滚动的情境下，需要能在移动端app进行展示的表格，特殊要求有要求表格表头、数据第一列进行固定。
- 实现：参照 element-ui 实现，表头<thread>与 <tbody>进行滚动分离实现表头的固定。使用一个长度为一列宽度的表格在<tbody>横向滚动时显示并显示 box-shadow 阴影，实现数据第一列固定
- 优化: 减少 dom 查询 复用查询节点。

 translate3d 可以开启硬件加速
为什么要用 translate3d 代替 overflow: scroll
1. 之前部分浏览器不支持 overflow 。
2. translate3d 可以开启硬件加速
3. translate3d 比起 margin position 只会 reflow 不会 retain

```html
<div class="lb-reportTotal-table-fixed lb-statistical-table-fixed" ng-show="!selectFilter">
    <table class="lb-table lb-reportTotal-table" style="min-width: 700px;position: relative;z-index: 5;">
        <thead>
            <tr>
                <th class="lb-table__cell" ng-repeat="head in tableHeadList" colspan="1" rowspan="1">
                    <span class="lb-table_cell-span" ng-style="{ 'width': head.width ? head.width : '100px' }"
                        ng-click="tableHeadSpanClickHandle($event, $index, head)">
                        <span>{{head.label}}</span>
                        <span ng-if="$index === 0" data-iconType="dropdowmicon"
                            class="lb-reportTotal-table-dropdownicon">
                            <i data-iconType="dropdowmicon" class="icon ion-arrow-down-b"
                                ng-class="{ 'ion-arrow-right-b': dropdownActive }"
                                ng-style="{ 'color' : dropdownSortAciton ? '#00a3f0' : '' }"></i>
                        </span>
                        <span ng-if="$index !== 0" data-iconType="sortIcon" class="lb-reportTotal-table-sortIcon">
                            <i class="icon ion-arrow-up-b" data-iconType="sortIcon" style="top: -4px;"
                                ng-style="getColomnSortStyle('asc',$index)"></i>
                            <i class="icon ion-arrow-down-b" data-iconType="sortIcon" style="top: 2px"
                                ng-style="getColomnSortStyle('desc',$index)"></i>
                        </span>
                    </span>
                </th>
            </tr>
        </thead>
    </table>
    <table class="lb-table lb-reportTotal-table lb-statistical-table-body" id="lb-reportTotal-table-fixed-tbody"
        style="position: relative;z-index: 4;min-width: 700;">
        <tbody>
            <tr ng-repeat="sale in salesList" ng-init="outerIndex=$index">
                <td ng-repeat="head in tableHeadList" class="lb-table__cell" rowspan="1" colspan="1">
                    <span class="lb-table_cell-span"
                        ng-style="{ 'width': head.width ? head.width : '100px' }">
                        <span ng-if="head.type === 'normal'">{{sale[head.value] || 0}}</span>
                        <span ng-if="head.type === 'date'">{{getTableCellTime(sale[head.value])}}</span>
                    </span>
                </td>
            </tr>
        </tbody>
    </table>
</div>
```

$scope.allSaler.unshift({val: 0, text: '未归属'});

# 开发流程： 
1. 切换到 master 分支并拉取远程代码。

2. 从 master 新建本地开发分支并切换到新分支。

3. 在分支上开发提交打包。

4. 明确开发思路开发顺序。

5. 开始开发。将 tb 任务移动到开发中。



# angularjs 的特性


# 场景
- js 如何判断图片的大小

- webapp 如何将图片缓存在本地


```js
// 解决 vue 项目调试不方便问题
const index = this.currentUrl.indexOf('#');
if (process.env.NODE_ENV === 'development' && index !== -1) {
    window.open("http://localhost:63342/" + this.currentUrl.slice(index), '_self');
    return;
}
```

2021/12/28  
库位设置完以后刷新商品列表

2021/12/29  
pc 库位开发
采购单附件提升质量

-生意通app

2021/1/7
为 gis-vue 引入友盟埋点

2022/1/14
修复生意通app多图分享bug
修复进销存app首页跳转无效bug
进销存Pc库位迁移
2022/1/15
进销存生意通app库位UI优化
进销存PC库位迁移
2022/1/18
进销存app、生意通app库位查询分页,商品详情显示维度bug修复

2022/1/22
进销存、生意通app
noticebirthday 分支修复
营销中设置了短信在生日当天定时发送，但是有一些的却没有发送。

待移入release

<table>
    <tr>
        <td>日期</td>
        <td>功能</td>
        <td>分支名</td>
        <td>是否合并</td>
        <td>端口</td>
    </tr>
    <tr>
        <td>2022/1/22</td>
        <td>营销中设置了短信在生日当天定时发送，但是有一些的却没有发送。</td>
        <td>noticebirthday</td>
        <td>1</td>
        <td>进销存、生意通app</td>
    </tr>
    <tr>
        <td>2022/1/22</td>
        <td>侧边栏图标删除</td>
        <td>delicon</td>
        <td>1</td>
        <td>生意通app</td>
    </tr>
    <tr>
        <td>2022/1/22</td>
        <td>单据价格同步</td>
        <td>syncpurchase</td>
        <td>1</td>
        <td>进销存app</td>
    </tr>
    <tr>
        <td>2022/2/11</td>
        <td>进销存app用户配置页面，提示语优化</td>
        <td>usersetting</td>
        <td>1</td>
        <td>进销存app</td>
    </tr>
    <tr>
        <td>2022/2/11</td>
        <td>Ipad登录进销存一直在启动页面卡住</td>
        <td>localstorageOversize</td>
        <td>2</td>
        <td>进销存app</td>
    </tr>
    <tr>
        <td>2022/2/11</td>
        <td>没有销售统计权限时，在商品详情页拿货统计图标指向了库存量tab（DEV-18454



）</td>
        <td>scantips</td>
        <td>2</td>
        <td>进销存app</td>
    </tr>
    <tr>
        <td>2022/2/11</td>
        <td></td>
        <td></td>
        <td>2</td>
        <td>进销存app</td>
    </tr>
</table>



https://gitlab.app.qinsilk.com/qinsilk/qinsilkApp/merge_requests/4417

【fix】Ipad登录进销存一直在启动页面卡住;防止localstorage超过5m时引起程序中断;

https://gitlab.app.qinsilk.com/qinsilk/qinsilkApp/merge_requests/4418  
【fix】没有销售统计权限时，在商品详情页拿货统计图标指向了库存量tab