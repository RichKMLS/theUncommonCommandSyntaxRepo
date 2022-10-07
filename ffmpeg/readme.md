# ffmpeg

- crop a video file and/or convert video file formats<br>

  <code> ffmpeg -i [input.video] -filter:v "crop=[xa]:[ya]:[x0]:[y0]" -s [xb]x[yb] -c:a copy [output.video] </code> <br>

> [xa], [ya] : dimensions of the video that you would like to crop out
> [x0], [y0] : defines the new 0 point for [xa] and [ya]
>
> (-s [xb], [yb] : resize cropped video : optional)

<br><br>

- screen record based on coordinates 

  <code>ffmpeg -video_size 100x100 -framerate 25 -f x11grab -i :0.0+200,300 output.mp4 </code> <br>
  
 > example 100x100 video shifted 200x and 300y at 25 fps
