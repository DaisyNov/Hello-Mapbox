# Hello-Mapbox

hello mapbox（all）
添加一些常见的地图控件，导航（NavigationControl，放大、缩小以及指北针按钮）、定位(GeolocateControl)、比例尺(ScaleControl)、全屏(FullscreenControl)：
标记和气泡都可以单独指定坐标添加到地图上。标记可以通过setPopup方法设置点击显示的气泡。对于标记，指定的坐标在标记图片中心点处，所以竖直方向需要偏移图片高度的一半，使指定的坐标在水滴形标记图片的尖端处；对于气泡，指定的坐标在气泡下部尖端处，所以偏移了标记图片的高度加1像素使气泡指向标记顶部。
  MapboxGL绘制点线面的方式其实和加载地图是一样的，点线面数据是放在数据源(source)里的，绘制时添加图层(layer)并指定数据源、显示参数等。
  
hello mapbox（original）
第一个MapboxGL程序：展示一幅地图
Map对象是MapboxGL的核心对象，地图的展示、交互等都由它来实现。上述代码中id为map的div元素为地图的容器；mapboxgl.Map构造方法用于创建Map对象，一个Map对象对应一个地图容器，参数container指定使用的地图容器id，style用于指定使用的Mapbox地图。
