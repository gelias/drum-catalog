# Drum Catalog

Catálogo de músicas para estudar bateria, com partitura, vídeo do YouTube e acompanhamento visual. A primeira música é **T.N.T. — AC/DC**.

## Estrutura

- `index.html`: página inicial com busca por música, artista ou estilo.
- `catalogo.json`: lista das músicas e seus metadados.
- `assets/`: aparência e comportamento do catálogo.
- `musicas/tnt-acdc/`: player, sincronização e imagens da primeira música.

Site estático, sem instalação de dependências, banco de dados ou etapa de compilação. Todos os caminhos são relativos, compatíveis com o endereço de projeto do GitHub Pages.

## Publicação

Em **Settings → Pages**, use **Deploy from a branch**, branch **main**, pasta **/(root)**. Cada atualização nessa branch publica uma nova versão. O arquivo `.nojekyll` permite servir os arquivos estáticos diretamente.

## Executar localmente

```sh
python3 -m http.server 8765 --bind 127.0.0.1
```

Abra `http://localhost:8765`. Abra pelo servidor ou pelo GitHub Pages para que o player do YouTube receba a identificação de origem necessária. Abrir por `file://` pode causar erro 153.

## Adicionar uma música

1. Crie uma pasta própria dentro de `musicas/`, por exemplo `musicas/nova-musica/`.
2. Adicione sua página `index.html` e os arquivos que ela utiliza.
3. Acrescente um item em `catalogo.json`, seguindo o formato do primeiro item: `id`, `titulo`, `artista`, `estilo`, `bpm`, `compasso`, `trechos`, `duracao`, `pagina` e `video`.
4. Envie as alterações ao GitHub. O cartão aparece automaticamente no catálogo.

## Edições e acompanhamento

As edições de títulos, anotações e ajustes de tempo são salvas apenas no navegador que fez a alteração. Não alteram o repositório e não são compartilhadas entre dispositivos. Substituições de imagem podem ser guardadas pelo botão **Salvar HTML editado**, que gera uma cópia independente. Para mudar a versão publicada, atualize os arquivos do repositório.

O marcador usa referências visuais do vídeo a cada cinco segundos e interpolação entre as referências. É um auxílio de estudo, com precisão aproximada; não é uma transcrição de cada ataque individual. O ajuste global permite adiantar ou atrasar o acompanhamento.

O vídeo é reproduzido pelo player do YouTube; não é armazenado neste repositório. Partituras e imagens da música foram fornecidas pelo usuário. Nenhuma licença de redistribuição dessas obras é concedida por este projeto.
