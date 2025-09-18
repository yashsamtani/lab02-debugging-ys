Name (solo): Yash Samtani

Link: https://www.shadertoy.com/view/wc2fzR

Bug #1: In line 95 of image, we declare vec instead of vec2 - fixed by just changing this, and found this by just compiling the code and seeing the syntax error on that line.

Bug #2: Instead of passing uv2 into the raycast function, we pass uv -> for this, it was fairly close to the first error, and I saw the logical error with raycasting.

Bug #3: We were doing H *= len * iResolution.x / iResolution.x;, which just equals 1 -> we should instead divide by y. I found this by seeing there was an issue with the image being incorrectly stretched/compressed.

Bug #4: Reflect uses eye instead of dir -> I just noticed the balls were not reflecting the floor as intended, and tried to look for reasons why.

Bug #5: Increase the number of march steps from 64 to 640 -> renders much more of the floor.
