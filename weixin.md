
# 微信小程序

## 一、生命周期


| 属性     | 描述    |  触发时机  |
| :-----:  | :-----:   | :----: |
|onLoad    | 监听页面加载 | 页面初始化  （只执行一次）  |
|onShow   | 监听页面显示 | 页面显示进入前台    |
|onReady   | 监听页面初次渲染完成 | 页面渲染完成  （只执行一次）  |
|onHide   | 监听页面隐藏 | 页面离开进入后台    |
|onUnload   | 监听页面卸载 | 页面销毁的时候  （只执行一次）   |
|onPullDownRefresh   | 监听用户下拉动作 | 下拉触发    |
|onReachBottom   | 页面上拉触底 | 上拉触发    |
|onShareAppMessage   | 用户点击右上角分享 | 分享的时候    |


## 二、路由的跳转

| 方法     | 描述    |  使用说明 |
| :-----:  | :-----:   |  :-----:   | 
|wx.switchtab(Object object)    | 跳转到 tabBar 页面，并关闭其他所有非 tabBar 页面 | wx.switchTab({url: '/index'}) 。路径后不能带参数 |
|wx.reLaunch(Object object)    | 关闭所有页面，打开到应用内的某个页面 | wx.reLaunch({url: 'test?id=1'}) 。路径后可以带参数|
|wx.redirectTo(Object object)    | 关闭当前页面，跳转到应用内的某个页面。但是不允许跳转到 tabbar 页面。 | wx.redirectTo({url: 'test?id=1'}) 。路径后可以带参数|
|wx.navigateTo(Object object)    | 保留当前页面，跳转到应用内的某个页面。但是不能跳到 tabbar 页面。使用 wx.navigateBack 可以返回到原页面。小程序中页面栈最多十层。 | wx.navigateTo({url: 'test?id=1'}) 。路径后可以带参数|
|wx.navigateBack(Object object)    | 关闭当前页面，返回上一页面或多级页面。可通过 getCurrentPages 获取当前的页面栈，决定需要返回几层。 | wx.navigateBack({delta: 2}) 返回的页面数，如果 delta 大于现有页面数，则返回到首页。 |
