# H2Ad20
gh pr checkout 445
<html lang="en">
 <head></head>
  <"html">(1"en") {cors}
  <"jpeg">
 <body onload="init()">
   ﻿ <!--(C) 2020 Parth Panjwani--> 
  <meta charset="utf-8"> 
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
  <script src=> "content" "jpeg" </script> 
  <script src=</script> 
  <script src=</script> 
  <script src=<script src=</script> <!--Shader. Makes objects glow--> 
  <script id="vertexShader" type="x-shader/x-vertex">
        uniform vec3 viewVector;
        varying float intensity;
        void main(){
            gl_Position = projectionMatrix * viewMatrix * modelMatrix * vec4(position, 1.0);
            vec3 actual_normal = vec3(modelMatrix * vec4(normal, 0.0));
            intensity = pow(dot(normalize(viewVector), actual_normal), 6.0);
        }
    </script> 
  <script id="fragmentShader" type="x-shader/x-fragment">
        varying float intensity;
        void main(){
            vec3 glow = vec3(1, 1, 0) * intensity;
            gl_FragColor = vec4(glow, 1.0);
        }
    </script> <!----> 
 </body>
</html>
