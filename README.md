Llevo tiempo usando la unidad de medida REM. Con el paso del tiempo me voy dando cuenta que no lo estaba usando siempre correctamente. Normalmente venía usándolo para tipofragías, margin y paddings

El usuario de la web puede tener configurado en su dispositivo un aumento (o disminución) del tamaño de la tipografía

No estableciendo la unidad de medida para tipografías en valores fijos (px, pt, cm...) le permiteremos al usuario que pueda personalizar el tamaño de la fuente. Yo particularmente prefiero usar REM frente a EM ya que con REM el valor relativo de partida siempre será la raiz (&lt;html&gt;), con EM será el elemento padre (en cascada) que tenga definida el tamaño de tipografía pudiéndose obtener valores relativos no esperados

Pero volviendo al inicio de esta entrada, ¿porque estaba usando mal los REMs?. Porque lo usaba para paddings y margins. Si el usuario tiene aplicado aumento de tipofrafía también afecta a estos atributos. Esto quiere decir que aumenta los espaciados, y en el caso de los paddings resta espacio para los contenidos: textos, imágenes, iconos...

Mejor con un ejemplo: https://codepen.io/ivan_albizu/pen/LYmaZyb y si usas Chrome, una manera rápida de cambiar el tamaño de la tipo es: chrome://settings/appearance

Puedes ver tres casos. En todos usamos la tipografía con REM para que pueda escalarse por el usuario. En el primer caso los padding, margins y border-width están con REM. En el segundo caso están fijados con PX. Y en el tercer caso una combinación de las anteriores min(XXpx, XXrem) para que si el usuario hace disminuir la tipografía no queda una tipografía muy pequeña con espaciados grandes. Esto ya lo dejo que investigues con otras combinaciones, como CLAMP() :)

Otro caso que puede requerir una pensada es la unidad de medida a usar en las @media, pero esto te lo dejo para tí, que has leído todo y llegado al final :)
