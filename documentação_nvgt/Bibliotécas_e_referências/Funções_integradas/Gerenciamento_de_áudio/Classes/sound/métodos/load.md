# load
Carrega um arquivo de som com as configurações especificadas.

1. `bool sound::load(string filename, pack@ soundpack = null, bool allow_preloads = true);`
2. `bool sound::load(sound_close_callback@ close_cb, sound_length_callback@ length_cb, sound_read_callback@ read_cb, sound_seek_callback@ seek_cb, string data, string preload_filename = "");`

## Parâmetros (1):
* string filename: O nome e caminho do arquivo que será carregado.
* pack@ soundpack = null: um identificador para o objeto do qual carregar este som, se houver.
* bool allow_preloads = true: verifica se o sistema deve ou não pré-carregar sons na memória durante a execução do jogo.

## Parâmetros (2):
* sound_close_callback@ close_cb: O próximo retorno de chamada a ser utilizado com o som.
* sound_length_callback@ length_cb: Indica a duração do retorno de chamada a ser associado ao som.
* sound_read_callback@ read_cb: O retorno de chamada de leitura a ser utilizado com o som.
* sound_seek_callback@ seek_cb: O retorno de chamada de busca a ser utilizado com o som.
* string data: os dados de áudio contidos no som.
* string preload_filename = "": o nome do arquivo a ser pré-carregado, se houver.

## Retorno:
bool: Verdadeiro se o som foi carregado com sucesso; Caso contrário, falço.

## Algumas observações:
A sintaxe para sound_close_callback é:
> void sound_close_callback(string user_data);

A sintaxe para sound_length_callback é:
> uint sound_length_callback(string user_data);

A sintaxe para sound_read_callback é:
> int sound_read_callback(string &out buffer, uint length, string user_data);

A sintaxe para sound_seek_callback  é:
> bool sound_seek_callback(uint offset, string user_data);
