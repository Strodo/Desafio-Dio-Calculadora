# Desafio-Dio-Calculadora
function calcularNivelRankeadas(vitorias, derrotas) {
    // Calcula o saldo de Rankeadas (vitórias - derrotas)
    const saldoVitorias = vitorias - derrotas;

    // Determina o nível com base no saldo de vitórias
    let nivel;
    if (vitorias < 10) {
        nivel = "Ferro";
    } else if (vitorias <= 20) {
        nivel = "Bronze";
    } else if (vitorias <= 50) {
        nivel = "Prata";
    } else if (vitorias <= 80) {
        nivel = "Ouro";
    } else if (vitorias <= 90) {
        nivel = "Diamante";
    } else if (vitorias <= 100) {
        nivel = "Lendário";
    } else {
        nivel = "Imortal";
    }

    // Retorna o resultado
    return `O Herói tem saldo de ${saldoVitorias} está no nível de ${nivel}`;
}

// Teste da função com diferentes valores de vitórias e derrotas
const mensagem = calcularNivelRankeadas(60, 20);
console.log(mensagem); // Exibe: "O Herói tem saldo de 40 está no nível de Ouro"
