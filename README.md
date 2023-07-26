This sample is created for issue https://github.com/flutter/flutter/issues/131186

it is not hard to reproduce this issue.

1、create a sample project :

flutter create app_size_sample

flutter build web 

the output file (main.dart.js) in build/web/   size is 1.4m 

2、add go_route dependency :

go_router: ^9.0.0

add code :

<img width="765" alt="image" src="https://github.com/flutter/flutter/assets/6874049/de2922f0-893c-4d0d-8ef4-1a053c711bd6">

now run 'flutter build web'

the output file (main.dart.js) in build/web/   size is 1.8m 

-----------------------detail--------------------------------------------------------------------------------------

Before import go_route :

<img width="478" alt="image" src="https://github.com/flutter/flutter/assets/6874049/79f21611-ce3b-4447-95d1-fd986d65a810">
<img width="1065" alt="image" src="https://github.com/flutter/flutter/assets/6874049/ff26fc9d-045a-442b-8da1-177a348a5751">


After import go_route :

<img width="718" alt="image" src="https://github.com/flutter/flutter/assets/6874049/f702f16e-7728-465d-9f34-7be6174fede6">

<img width="462" alt="image" src="https://github.com/flutter/flutter/assets/6874049/176b72da-0cfb-4c14-b37c-d9eafec2e121">
<img width="1083" alt="image" src="https://github.com/flutter/flutter/assets/6874049/2f915a3d-c92b-4431-9c3d-e16ff3cbdd2f">
