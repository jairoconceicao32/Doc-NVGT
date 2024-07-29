/**
	Fecha um som que está aberto, disponibilizando um novo objeto de som para ser recarregado.
	bool sound::close();

	## Algumas observações:
		bool: verdadeiro se o som puder ser fechado; Caso contrário, falço, por exemplo se não houver nenhum som aberto.
*/

// Exemplo:
void main() {
	sound s;
	s.load("C:/windows/media/ding.wav");
	alert("Exemplo", s.close()); // Será mostrado como verdadeiro, pois um som foi aberto anteriormente.
	alert("Exemplo", s.close()); // Agora ele exibirá falso, pois a operação anterior removeu qualquer som previamente anexado ao objeto de som.
}
