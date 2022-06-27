# ffmpeg

- crop a video file and/or convert video file formats<br>
 <code> ffmpeg -i [input.video] -filter:v "crop=[xa]:[ya]:[x0]:[y0]" -s [xb]x[yb] -c:a copy [output.video] </code> <br>

> [xa], [ya] : dimensions of the video that you would like to crop out
> [x0], [y0] : defines the new 0 point for [xa] and [ya]
>
> (-s [xb], [yb] : resize cropped video : optional)
