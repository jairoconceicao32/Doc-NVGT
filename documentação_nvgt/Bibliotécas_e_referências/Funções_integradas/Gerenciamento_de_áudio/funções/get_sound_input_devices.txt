/**
	Retorna um array de strings listando todos os dispositivos de áudio de entrada que estão disponíveis no sistema.
	string[]@ get_sound_input_devices();


	## Retorno:
		string[]@: Um identificador para um array que lista todos os dispositivos de entrada disponíveis.

	## Algumas observações:
		Depois de listar os dispositivos com essa função, podemos definir a propriedade global do mecanismo usando sound_input_device para qualquer índice no array retornado que contenha o nome do dispositivo que se deseja definir.
		Essa lista sempre irá incluir um dispositivo sem som. Se quisermos que o usuário não possa celecionar, podemos ficar a vontade para não permitir que ele mova o cursor entre os dispositivos, ou podemos não adicionálo ao nossos menus, etc. No entanto, devemos estar atentos à diferença de índice que isso pode causar ao definirmos a propriedade sound_output_device. Por exemplo, é crucial lembrar que sound_output_device=0 configura o sistema para nenhum som, enquanto sound_output_device=1 define o primeiro dispositivo real no sistema ou o dispositivo padrão.
*/

// Exemplo:
void main() {
	string[]@ dispositivos = get_sound_input_devices();
	dispositivos.remove_at(0); // Don't allow the user to select no sound.
	alert("Dispositivos", "Os seguintes dispositivos estão disponíveis em seu sistema: " + join(dispositivos, ", "));
}
