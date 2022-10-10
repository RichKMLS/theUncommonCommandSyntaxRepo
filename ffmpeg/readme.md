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


<br><br>

- convert a video into a high quality gif with a low file size

  <code>vin="vid.mp4"; gout="output.gif"; ffmpeg -i vin -vf palettegen palette.png; wait; \ </code>
  
  <code>ffmpeg -i $vin -i palette.png -filter_complex "fps=30,scale=600:-1:flags=lanczos[x];[x][1:v]paletteuse" -y $gout</code>
