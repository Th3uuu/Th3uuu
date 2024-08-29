-// Base de dados de filmes (exemplo simples)
const filmes = [
    { titulo: "O Poderoso Chefão", genero: "Crime", ano: 1972, popularidade: 10 },
    { titulo: "Vingadores: Ultimato", genero: "Ação", ano: 2019, popularidade: 9 },
    { titulo: "Parasita", genero: "Drama", ano: 2019, popularidade: 8 },
    { titulo: "Star Wars: Episódio IV", genero: "Ficção Científica", ano: 1977, popularidade: 10 },
    { titulo: "A Origem", genero: "Ficção Científica", ano: 2010, popularidade: 9 },
    { titulo: "Matrix", genero: "Ficção Científica", ano: 1999, popularidade: 9 },
    { titulo: "Cidade de Deus", genero: "Crime", ano: 2002, popularidade: 10 },
    { titulo: "O Senhor dos Anéis: O Retorno do Rei", genero: "Fantasia", ano: 2003, popularidade: 10 },
    { titulo: "Pulp Fiction: Tempo de Violência", genero: "Crime", ano: 1994, popularidade: 9 }
];

// Função para recomendar filmes por gênero
function recomendarPorGenero(genero) {
    return filmes.filter(filme => filme.genero.toLowerCase() === genero.toLowerCase());
}

// Função para recomendar filmes por popularidade
function recomendarPorPopularidade(minPopularidade) {
    return filmes.filter(filme => filme.popularidade >= minPopularidade);
}

// Função para recomendar filmes lançados depois de um certo ano
function recomendarPorAno(minAno) {
    return filmes.filter(filme => filme.ano >= minAno);
}

// Exemplos de uso:
console.log("Recomendação por Gênero (Crime):");
console.log(recomendarPorGenero("Crime"));

console.log("\nRecomendação por Popularidade (maior que 9):");
console.log(recomendarPorPopularidade(9));

console.log("\nRecomendação por Ano (após 2000):");
console.log(recomendarPorAno(2000));
