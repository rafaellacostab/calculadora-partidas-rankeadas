// Função para calcular o nível do jogador com base nas vitórias e derrotas
function calcularNivel(vitorias, derrotas) {
    // Calculando o saldo de vitórias
    let saldoVitorias = vitorias - derrotas;

    // Inicializando o nível
    let nivel = "";

    // Definindo o nível baseado no saldo de vitórias
    if (vitorias < 10) {
        nivel = "Ferro";
    } else if (vitorias >= 10 && vitorias <= 20) {
        nivel = "Bronze";
    } else if (vitorias >= 21 && vitorias <= 50) {
        nivel = "Prata";
    } else if (vitorias >= 51 && vitorias <= 80) {
        nivel = "Ouro";
    } else if (vitorias >= 81 && vitorias <= 90) {
        nivel = "Diamante";
    } else if (vitorias >= 91 && vitorias <= 100) {
        nivel = "Lendário";
    } else if (vitorias >= 101) {
        nivel = "Imortal";
    }

    // Imprime a mensagem com o saldo e o nível do jogador
    print(`O Herói tem de saldo de ${saldoVitorias} está no nível de ${nivel}`);
}

// Entrada de dados
let vitorias = parseInt(gets()); // Número de vitórias
let derrotas = parseInt(gets()); // Número de derrotas

// Chamada da função para calcular e exibir o nível
calcularNivel(vitorias, derrotas);
