
# Bug/Error 
- [x] **一定会出现** 会将```iResolution```转换为1，这将直接导致错误
  - 在变量区加上```uniform vec3 iResolution; ```即可

- [ ] **一定会出现** 将OpenGL的```Texture```转换为HLSL的```tex2Dlod```方法时出错，因为[TextureLod](https://registry.khronos.org/OpenGL-Refpages/gl4/html/textureLod.xhtml)是3个参数，而[tex2Dlod](https://learn.microsoft.com/en-us/windows/win32/direct3dhlsl/dx-graphics-hlsl-tex2dlod)是2个参数

- [x] **偶尔出现** 会缺失```}```
  - 这好办，Unity会直接提示语法错误，加上就可以了

- [x] **偶尔出现** 将```MainImage```转换为片元着色器时，可以没有```return```,因为ShaderToy的```MainImage```的最后一行一般是```fragColor = vec4()``` 
- [x]  可能会出现重复生成的情况，比如```fixed3 init = fixed3(sin(time * .0032, sin(time * .0032, sin(time * .0032) * .3, .35 - cos(time * .005) * .3, time * 0.002);```中重复生成了```sin(time * .0032```
- [x]  ```END CG```位置可能出现错误，放在了函数里面 
- ![ENDCG位置错误](Images/Issues/ENDCG位置错误.png)
  - 解决办法：
    - 一般手动下移一行即可
    - 并且要注意一般会在代码末尾少一个```}```

- 案例 少括号 小数点变成了逗号 不允许向量直接减去数字
  ![案例1](./Images/Issues/少括号%20小数点变成了逗号%20不允许向量直接减去数字.png)
  - **频繁出现** <font color="00ffff">少括号</font> 
  - **偶尔出现** <font color="00ff00">小数点变成了逗号</font>  这个```.```是如何被错误的转换为```,```，着实无法理解
  - **绝对会出现** <font color="ffff00">不允许向量直接减去数字</font> ，在GLSL中是允许这样操作的，但是Unity/HLSL是不支持的


