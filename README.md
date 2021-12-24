# Animação de conclusão
Disparar animação em canvas com CreateJS após a conclusão de alguma tarefa. A animação foi construída com o Adobe Animate que renderiza em um arquivo javascript para exibição numa tag canvas
## Pastas e Arquivos
- Pasta images - Contém as imagens geradas pelo Adobe Animate para a animação na tag canvas
- conclusao_style.css  - Estilização para o recipiente da animação
- Arquivos JS obrigatórios para o funcionamento do processo (declarar antes de /body ) <br/> 
Exemplo (os arquivos deverão ser carregados nessa ordem):<br/>
<script src="https://code.createjs.com/1.0.0/createjs.min.js"></script> <br/>
<script src="anim_finish.js"></script> <br/>
<script src="conclusao_atividade.js"></script> <br/>

## Dicas
- No final do arquivo HTML insira a seguinte as seguintes tags com a animação no canvas:<br>
<div id="finish_animation_container" style="background-color:rgba(255, 255, 255, 0.00); width:1920px; height:1080px">
		<canvas id="canvas" width="1920" height="1080" style="position: absolute; display: block; background-color:rgba(255, 255, 255, 0.00);"></canvas>
		<div id="dom_overlay_container" style="pointer-events:none; overflow:hidden; width:1920px; height:1080px; position: absolute; left: 0px; top: 0px; display: block;">
		</div>
    </div><br />
- Escreva o seu código, faça a sua atividade e quando precisar que a animação seja processada utilize o seguinte método: <br/>
play_animaconclusao(); <br/>
- Se for gerar uma nova animação pelo Adobe Animate renomeie todos os termos "animation_container" para "finish_animation_container"
- Para uma melhor organização você pode utilizar uma subpasta como "finish_animation" e fazer o carregamento dos arquivos JS desssa forma:<br>
<script src="https://code.createjs.com/1.0.0/createjs.min.js"></script> <br/>
<script src="finish_animation/anim_finish.js"></script> <br/>
<script src="finish_animation/conclusao_atividade.js"></script> <br/>


## Exemplo
O arquivo index.html tem uma atividade onde o usuário precisa clicar na resposta correta, ao fazer isso o método play_animaconclusao();
dispara a animação de conclusão.

## Vantagens
A animação é no formato vetorial, dessa forma não haverá perda de resolução se a área da animação for ampliada e o loading da animação acontece após o carregamento do DOM. Antes da conclusão da atividade, a animação estará carregada e pronta para rodar.
