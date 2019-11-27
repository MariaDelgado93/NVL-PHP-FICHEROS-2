<?php

reemplazar('quijote.txt', 'quijote-modificado.txt', 'Sancho', 'Morty');

function reemplazar($ficheroorig,$ficheronuevo,$patron,$sustitucion){
  $descriptor = fopen('$ficheroorig','r');
  while (($contenido = fgets($descriptor)) !== false){
    $modified = str_replace($patron, $sustitucion, $contenido);
    $fd = fopen('$ficheronuevo','w');
    fwrite($fd,$modified);
  }
}
