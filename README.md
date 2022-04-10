# Jogo da Velha
O jogo da velha consiste em uma disputa entre dois jogadores para formar uma sequencia em linha reta dos simbolos "X" ou "Circulo", e no caso de nenhuma sequência
ser concluída ocasiona-se um empate, também chamado de "Velha".

## Tecnologias Utilizadas 
- **HTML**: estrutura do site
- **CSS**: Estilização do site 
- **JAVASCRIPT**: Funções do site

### Melhorias possiveis
1. [ ] Utilizar o BoosTrap
2. [ ] Deizar responsivo
3. [ ] Adicionar sons 
4. [ ] Adicionar sistema de pontução
5. [ ] Opções de tema para o tabuleiro 

### Disponibilizar em
[GitHub Page](https://danielsanchs.github.io/Jogo_Da_Velha_X_Daniel-/)

#### Prints da Tela
 | id | primeira tela | Segunda tela |
 |----|---------------|--------------|
 | 1 | inicio de um jogo | Final do jogo |
 | 2 | ![image](https://user-images.githubusercontent.com/92760821/162595611-64a0314d-be19-4b42-af5c-9a86a546dea7.png) | ![image](https://user-images.githubusercontent.com/92760821/162595631-9150e59d-1c18-4ae0-8772-0e8694fcf56d.png) |
 
 ### Função Principal 
 ```JS:
function botao(ctx, j){
    if(!travado){
        while(tabelaJogo[j] == 0){
            if(jogador == "Jogador 1"){
                ctx.beginPath();
                ctx.moveTo(20,20);
                ctx.lineTo(180,180);
                ctx.moveTo(180,20);
                ctx.lineTo(20,180);
                ctx.lineWidth = 30;
                ctx.strokeStyle = "black";
                ctx.stroke();
                tabelaJogo[j] = 1;
                cont++;
                testeVitoria();
                jogador = "Jogador 2";
            }else{
                ctx.beginPath();
                ctx.arc(100,100,70,0,2*Math.PI);
                ctx.strokeStyle = "black";
                ctx.lineWidth = 30;
                ctx.stroke();
                tabelaJogo[j] = 2;
                cont++;
                testeVitoria();
                jogador = "Jogador 1";
            }
        }
    }
}
 ```
 
 ### Comando Git
Para iniciar o projeto 
```bash:
git init
```
Para fazer um commit
```
git add *
git commit -m "Mensagem do commit"
git push -u origin master
