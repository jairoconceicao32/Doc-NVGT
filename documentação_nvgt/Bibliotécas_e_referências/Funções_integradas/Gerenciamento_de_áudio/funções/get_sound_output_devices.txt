/**
	Retorna um array de strings listando todos os dispositivos de saída disponíveis no sistema.
	string[]@ get_sound_output_devices();

	## Retorno:
		string[]@: Um identificador para um array que lista todos os dispositivos de saída disponíveis.

	## Algumas observações:
		Depois de listar os dispositivos com essa função, podemos definir a propriedade global do mecanismo sound_output_device para qualquer índice do array retornado que contenha o nome do dispositivo que desejamos definir.
		This list will always include a no sound device. If you don't want the user to be able to select it, feel free to not allow them to move their cursor to that item or not add it to your menus etc, but remember to pay attention to the index difference this may create when setting the sound_output_device property, namely just remember that setting sound_output_device = 0 will set the system to no sound, and setting the device to 1 will always be the first real device in the system, or the default device at least on windows.
*/

// Example:
void main() {
	string[]@ devices = get_sound_output_devices();
	devices.remove_at(0); // Don't allow the user to select no sound.
	alert("devices", "The following devices are installed on your system: " + join(devices, ", "));
}
