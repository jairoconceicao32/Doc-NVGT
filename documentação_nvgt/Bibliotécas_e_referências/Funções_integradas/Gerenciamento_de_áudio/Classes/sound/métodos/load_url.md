/**
	Carrega uma URL especificada.
	bool sound::load_url(string url);

	## Parâmetros:
		* string url: A URL a ser carregada (deve ser um link direto para um som ou stream).

	## Returns:
		Bool: Verdadeiro se a URL foicarregada com sucesso; Caso contrário falço.
*/

// Exemplo:
void main() {
	sound s;
	bool success = s.load_url("https://example.com/my_sound.mp3");
	alert("Resultado", "O som era " + (success == false? "não " : "") + "Carregado com sucesso.");
}
