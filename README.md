Основано на [st](https://st.suckless.org) с suckless.org

Это мой "форк" st с патчами, поддержкой конфигурации
во время запуска и нужными мне патчами.  
Зависит от [e1l](https://etar125.ru/e1l) (пока что).

Применённые патчи:
- alpha
- clipboard
- bold is not bright
- csi 22, 23
- blinking cursor
- fontmetrics
- background image

Поскольку патчи `alpha` и `background` image не совместимы,
я их разделил, поэтому можно выбрать только что-то одно.

Моя конфигурация (`~/.config/st/config.elist`):

```
font: gallant12:pixelsize=14:antialias=true:autohint=true
cwscale: 1.3
ignoreOS2metrics: 0
shell: /bin/bash
colors: #1b1d1e
       +#f92672
       +#82b414
       +#fd971f
       +#4e82aa
       +#8c54fe
       +#465457
       +#ccccc6
       +#505354
       +#ff5995
       +#b6e354
       +#feed6c
       +#0c73c2
       +#9e6ffe
       +#899ca1
       +#f8f8f2
fgcolor: #ffffff
bgcolor: #000000
alpha: 0.9
cursorstyle: 5
allowwindowops: 1
termname: xterm-256color
enablebg: 1
pseudotransparency: 1
bgfile: /home/etar125/def.ff
```

`alpha` будет игнорироваться, ведь `enablebg 1`.
`ignoreOSmetrics` и `cwscale` установлены для корректного отображения `gallant`,
другие шрифты вроде нормально и без этого отрисовываются.
