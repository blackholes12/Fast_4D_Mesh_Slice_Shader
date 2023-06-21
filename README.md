# 4d mesh slice vertex shader
Currently almost best way to generate 4d slice by vertex shader,which has generate 10000 4d objects in c++ environment by opengl in lower laptop at 30hz frame/s by me.If each 4d object has 50 tetras be used(if using texture or buffer to replace a bunch of "if" cases,one object can bind 500 tetras),it can generate 500,000 or  5,000,000(one object can run with 10,000,000 or 100,000,000 4d tetras) 4d tetras even more by valkan.So,it is a break through in dimension and quantity,it can be used in almost all game engines if you want.
## How to use it?
Lets consider the easiest way to generate a 4d tetra,you need at least(4 vec4 points and 1 uint id)struct be defined in cpu code as one tetra and copy and send 
4 tetras to the vertex shader with(id=0,id=1,id=2,id=3)(4 tetras' points are same),the indices is 0,1,2,0,2,3.
These 4 vec4 points need to be arranged in a certain order if you need single side mesh.
<img width="955" alt="2023-06-19 212647" src="https://github.com/blackholes12/Fast_4D_Mesh_Slice_Shader/assets/104487053/842f9496-ef83-4def-860e-320c16fa221d">


