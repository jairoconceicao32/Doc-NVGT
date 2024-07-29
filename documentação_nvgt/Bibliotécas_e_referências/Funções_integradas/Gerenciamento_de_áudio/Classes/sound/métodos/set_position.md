# set_position
Define a posição do som no espaço três-Dê.

`bool sound::set_position(float listener_x, float listener_y, float listener_z, float sound_x, float sound_y, float sound_z, float rotation, float pan_step, float volume_step);`

## Parâmetros:
* float listener_x: A posição x do ouvinte.
* float listener_y: A posição y do ouvinte.
* float listener_z: A posição Z do ouvinte.
* float sound_x: a posição x do som.
* float sound_y: a posição y do som.
* float sound_z: a posição z do som.
* float rotation: a rotação do ouvinte (em graus).
* float pan_step: a etapa de pan (por exemplo, quão extremo é o pan).
* float volume_step: a etapa de volume (muito semelhante a pan_step, mas para volume).

## Retorno:
bool: verdadeiro se a posição foi definida com sucesso; caso contrário, falso.
