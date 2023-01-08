
# web blogs
- [mapping-between-HLSL-and-GLSL](https://anteru.net/blog/2016/mapping-between-HLSL-and-GLSL/)


# functions
| HLSL                        | GLSL                  |
| --------------------------- | --------------------- |
| atan2(y,x)                  | atan                  |
| ddx                         | dFdx                  |
| ddx_coarse                  | dFdxCoarse            |
| ddx_fine                    | dFdxFine              |
| ddy                         | dFdy                  |
| ddy_coarse                  | dFdyCoarse            |
| ddy_fine                    | dFdyFine              |
| EvaluateAttributeAtCentroid | interpolateAtCentroid |
| EvaluateAttributeAtSample   | interpolateAtSample   |
| EvaluateAttributeSnapped    | interpolateAtOffset   |
| frac                        | fract                 |
| lerp                        | mix                   |
| mad                         | fma                   |
| saturate                    | clamp(x, 0.0, 1.0)    |



# System values & built-in inputs
| HLSL	|GLSL|
|---|---|
| SV_ClipDistance| gl_ClipDistance|
| SV_CullDistance| gl_CullDistance if ARB_cull_distance is present|
| SV_Coverage| gl_SampleMaskIn & gl_SampleMask|
| SV_Depth| gl_FragDepth|
| SV_DepthGreaterEqual	| layout (depth_greater) out float gl_FragDepth;|
| SV_DepthLessEqual	| layout (depth_less) out float gl_FragDepth;|
| SV_DispatchThreadID| gl_GlobalInvocationID|
| SV_DomainLocation| gl_TessCord|
| SV_GroupID| gl_WorkGroupID|
| SV_GroupIndex| gl_LocalInvocationIndex|
| SV_GroupThreadID| gl_LocalInvocationID|
| SV_GSInstanceID| gl_InvocationID|
| SV_InsideTessFactor| gl_TessLevelInner|
| SV_InstanceID| gl_InstanceID & gl_InstanceIndex (latter in Vulkan with different semantics)|
| SV_IsFrontFace| gl_FrontFacing|
| SV_OutputControlPointID| gl_InvocationID|
| N/A| gl_PatchVerticesIn|
| SV_Position| gl_Position in a vertex shader, gl_FragCoord in a fragment shader|
| SV_PrimitiveID| gl_PrimitiveID|
| SV_RenderTargetArrayIndex| gl_Layer|
| SV_SampleIndex| gl_SampleID|
| The equivalent functionality is available through EvaluateAttributeAtSample| gl_SamplePosition|
| SV_StencilRef| gl_FragStencilRef if ARB_shader_stencil_export is present|
| SV_Target	| layout(location=N) out your_var_name;|
| SV_TessFactor| gl_TessLevelOuter|
| SV_VertexID| gl_VertexID & gl_VertexIndex (latter Vulkan with different semantics)|
| SV_ViewportArrayIndex| gl_ViewportIndex |