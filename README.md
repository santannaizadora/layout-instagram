# Descrição

Seu segundo projeto será aplicar o layout responsivo da versão web do Instagram, utilizando HTML e CSS. Tente deixar sua página ao máximo parecida com o layout fornecido!

Desta vez há menos anotações. Explore o Figma e encontrará as medidas que não foram fornecidas em anotações.


# Requisitos

Sinta-se à vontade para colocar as fotos de exemplo que quiser no seu Instagram! :)

- Layout
    - [ ]  Aplicar layout para desktop, seguindo layout fornecido no figma
    - [ ]  Aplicar layout para mobile, seguindo layout fornecido no figma
    - [ ]  O layout sem sidebar deve ser ativado quando a largura da tela for menor que 935px
    - [ ]  O layout para mobile deve ser ativado quando a largura da tela for inferior a 614px
    - [ ]  Não é obrigatório que a sidebar fique fixa conforme o usuário desce na página como ocorre no Instagram (mas é um bônus)
- Ícones
    - [ ]  Utilize os ícones da biblioteca Ionicons: [https://ionicons.com/](https://ionicons.com/)
    
    A seção **Dicas** contém um tutorial para utilizar a biblioteca.
    
- Stories
    - [ ]  Na caixa dos stories, deve haver itens o suficiente para ultrapassar a largura, mas os itens a mais não devem ser exibidos, conforme layout
    - [ ]  Deve haver, no modo desktop, uma setinha no canto direito dos stories (conforme mostrado no layout do figma)
    - [ ]  A setinha não precisa funcionar ao clicar (só será possível quando vermos JavaScript)
    - [ ]  Não pode haver um scroll horizontal visível

# Dicas

- Ícones
    
    Ícones poderiam ser adicionados como imagens na página, mas usar imagens PNG e JPG podem fazer com que a imagem fique pixelizada se quisesse em tamanhos diferentes. Além disso, é muito difícil trocar a cor de imagens.
    
    Ao invés de usar imagens PNG ou JPG, poderíamos usar imagens no formato SVG, que podem ser customizadas por CSS e não tem um tamanho fixo. Uma imagem SVG é um arquivo como o seguinte:
    
    ```xml
    <svg xmlns='http://www.w3.org/2000/svg' class='ionicon' viewBox='0 0 512 512'>
    	<title>Heart</title>
    	<path d='M352.92 80C288 80 256 144 256 144s-32-64-96.92-64c-52.76 0-94.54 44.14-95.08 96.81-1.1 109.33 86.73 187.08 183 252.42a16 16 0 0018 0c96.26-65.34 184.09-143.09 183-252.42-.54-52.67-42.32-96.81-95.08-96.81z' fill='none' stroke='currentColor' stroke-linecap='round' stroke-linejoin='round' stroke-width='32'/>
    </svg>
    ```
    
    Mas colocar este código no nosso HTML acaba poluindo a página. Para evitar isso, foram feitas bibliotecas que escondem a complexidade do SVG. Neste projeto, utilizaremos a **Ionicons.**
    
    Com essa biblioteca, ao invés de inserir o SVG no nosso HTML, podemos inserir o seguinte:
    
    ```html
    <ion-icon name="heart-outline"></ion-icon>
    ```
    
    deixando seu código bem mais legível.
    
    *Uai, mas existe essa tag `ion-icon`!?*
    
    Não. Mas desenvolvedores escreveram um código Javascript que faz com que elas funcionem nos navegadores.
    
    *E como é que eu faço pra fazer isso funcionar na minha página?*
    
    Basta adicionar o seguinte **ao final** do seu `body`, antes de fechá-lo: 
    
    ```html
    <script src="https://unpkg.com/ionicons@5.4.0/dist/ionicons.js"></script>
    ```
    
    *Beleza. Mas e aí, como faço pra saber o que colocar no atributo `name`? Vou ter que ficar chutando??*
    
    Não! Todos os ícones desta biblioteca estão na página [https://ionicons.com/](https://ionicons.com/). Lá podemos encontrar todos os ícones com todas as suas variações (*outline* - só o contorno, *filled* - preenchido e *sharp*). Ao clicar em um ícone, o seguinte aparece no canto inferior da página.
    
    Agora, para inserir o ícone, podemos copiar o que está escrito no campo *WEB COMPONENT CODE* e colocar na nossa página.
    
    *Bacana! Mas você falou sobre customizar o ícone com CSS. Como faço isso?*
    
    Você pode alterar o tamanho do ícone alterando seu `font-size` e também pode alterar a cor com `color`. Você pode também consultar seus tutores para mais informações e dúvidas sobre a biblioteca :)
    
# Bônus

Bônus não são obrigatórios, mas caso tenha conseguido terminar todo o projeto antes do prazo, sugerimos fazer as seguintes funcionalidades:

- Vídeo
    - [ ]  Pelo menos um dos posts deve ser um vídeo
    - [ ]  Não é necessário ter o botão de play
    - [ ]  O vídeo deve ser inserido tanto no formato .mp4 e .ogg, para que funcione em qualquer navegador
    - [ ]  O vídeo deve ser iniciado automaticamente
    
    Nos arquivos úteis já tem um vídeo para facilitar essa parte :)
    
    Para não incomodar o usuário, os navegadores não permitem que um vídeo toque automaticamente a não ser que o som esteja desativado. Então, se colocou o atributo para iniciar o vídeo automaticamente e não funcionou, desative o som dele :)
    
- Sidebar fixa
    
    Se você acessar a página do Instagram do seu computador e descer na página, perceberá que a barra lateral continua visível, fixa na página.
    
    A ideia deste bônus é implementar este comportamento, fazendo que, ao descer na página, a coluna permaneça no mesmo lugar sempre.
    
- Comentários
    
    Pelos propósitos do projeto, não adicionamos os comentários dos posts no layout do Figma. Estes são os requisitos deste bônus:
    
    - [ ]  Ter comentários nos posts, com botão de like no canto direito em cada comentário
    - [ ]  Uma caixa para digitar o comentário, utilizando a tag `input`
    - [ ]  Um botão ao lado desta caixa para **Publicar**, com cor `#B2DFFC` inicialmente e, ao passar o mouse, fique com a cor `#0095F6` com uma transição que dura `300ms`. Procure pela propriedade *transition* para fazer isso :)
