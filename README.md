# jsDelivr 缓存刷新小工具

## CDN 缓存
jsDelivr 提供的全球 CDN 加速，CDN的分流作用不仅减少了用户的访问延时，也减少的源站的负载。但其缺点也很明显：当网站更新时，如果CDN节点上数据没有及时更新，即便用户再浏览器使用Ctrl +F5的方式使浏览器端的缓存失效，也会因为CDN边缘节点没有同步最新数据而导致用户端未能及时更新。 

CDN边缘节点对开发者是透明的，相比于浏览器Ctrl+F5的强制刷新来使浏览器本地缓存失效，开发者可以通过CDN服务商提供的“刷新缓存”接口来达到清理CDN边缘节点缓存的目的。这样开发者在更新数据后，可以使用“刷新缓存”功能来强制CDN节点上的数据缓存过期，保证客户端在访问时，拉取到最新的数据。 

## jsDelivr 缓存刷新方式
对于 jsDelivr，缓存刷新的方式也很简单，只需将想刷新的链接的开头的


https://cdn.jsdelivr.net/...
替换成
https://purge.jsdelivr.net/...  
即可实时刷新。刷新成功后，浏览器会返回缓存刷新成功的信息  

本工具基于该接口开发，你需要输入你想要刷新的jsDelivr链接，然后点击"刷新"即可，如不能刷新，可以多刷新几次






















