+++
title = 'Jetpack Compose'
date = 2023-11-16
tags= ['Android','Jetpack Compose']
+++

# Surface组件
Surface是Jetpack Compose的基本构建块之一。它是一个提供可视化空间以及处理高程、形状和边界的组件。Surface可以让开发人员控制阴影、边框、形状和背景色等元素的视觉效果。

影响Surface的属性

颜色（Color）：这是Surface背景的颜色。您可以传递任何颜色值。
形状（Shape）：这定义了Surface的边界形状。默认情况下，Surface是矩形的，但你可以使用内建的形状如CircleShape，或者创建自定义形状。
高程（Elevation）：这定义了Surface的高程（Z轴）。根据Material Design的规范，更高的Surface将投射更大的阴影。

@Preview
@Composable
fun surfaceTest(){
    Surface(color = Color.Yellow, modifier = Modifier.size(100.dp), shape = CircleShape, elevation = 15.dp) {
        Box(modifier = Modifier.fillMaxSize(), contentAlignment = Alignment.Center){
            Text(text = "Hello Word")
        }
 
    }
}