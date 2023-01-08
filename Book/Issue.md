
# Bug/Error 
- [ ] **一定会出现** 会将```iResolution```转换为1，这将直接导致错误

- [ ] **一定会出现** 将OpenGL的```Texture```转换为HLSL的```tex2Dlod```方法时出错，因为[TextureLod](https://registry.khronos.org/OpenGL-Refpages/gl4/html/textureLod.xhtml)是3个参数，而[tex2Dlod](https://learn.microsoft.com/en-us/windows/win32/direct3dhlsl/dx-graphics-hlsl-tex2dlod)是2个参数

- [ ] **偶尔出现** 会缺失```}```
  - 这好办，Unity会直接提示语法错误，加上就可以了

- [ ] **偶尔出现** 将```MainImage```转换为片元着色器时，可以没有```return```,因为ShaderToy的```MainImage```的最后一行一般是```fragColor = vec4()``` 
- [ ]  可能会出现重复生成的情况，比如```fixed3 init = fixed3(sin(time * .0032, sin(time * .0032, sin(time * .0032) * .3, .35 - cos(time * .005) * .3, time * 0.002);```中重复生成了```sin(time * .0032```
- [ ]  ```END CG```位置可能出现错误，放在了函数里面



