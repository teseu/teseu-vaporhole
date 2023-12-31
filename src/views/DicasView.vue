<script setup>
import Card from '@/components/ui/TheCard.vue'
 import Title from '@/components/ui/TheTitle.vue'
</script>

<template>
  <div class="flex flex-col mb-8">
    <div class="flex flex-col gap-4">
      <Title>
        <template #titulo>Dicas</template>
      </Title>
      <h2 class="text-3xl mb-4">Introdução</h2>
      <p class="text-base mb-4">
        Há diversas coisas para personalizar a interface do terminal e deixá-lo com a cara que vc quer,
        desde a escolha do emulador (são tantos e para tantos ambientes que fica difícil descrever) até a
        configuração oferecida por tal emulador.
      </p>
      <p class="text-base mb-4">
        Apesar de ser uma coisa que fiz muito, ainda faço, só que menos agora q tenho todos os meus emuladores já
        personalizados em algum ponto, ñ é o assunto proposto aqui nas dicas, até poderia fazer se sentisse q seria
        útil ou algo q o público dessa pág acha relevante.
      </p>
      <p class="text-base mb-4">
        Dito tudo isso, vou começar com os Prompt's, que usei o bash como exemplo, mas quase tudo é possível usar
        no fish tb. Digo quase tudo pq já me deparei com algumas exceções com o zsh pelo menos, principalmente ao
        usar o tmux, por isso, apesar de ter trocado pro zsh há algum tempo, o shell padrão do tmux no meu ambiente
        em casa é o bash.
      </p>
      <Card>
        <template #titulo>Interface</template>
        <h2 class="text-3xl mb-4">Prompt</h2>
        <p class="text-base mb-4">
          Na página About há alguns screenshots de como a tela ficou personalizando tanto o prompt qto o próprio tmux.
          Ali tem um pouco de tudo, um novo prompt, usando <a class="link" href="https://starship.rs/" target="_blank" >
            starship</a>, vários plugins para o tmux e alterações no .bashrc. Começando pelo prompt.
        </p>
        <p class="text-base mb-4">
          A instalação é bem simples do starship, de acordo com o sistema escolhido, sendo que para uso no vaporHole a opção é a
          instalação via curl, a 1ª q aparece se vc selecionar o Linux como sistema. A configuração depende muito de
          onde vc quer chegar, sendo q a personalização vc encontra dentro de <a class="link"
          href="https://starship.rs/presets/" target="_blank">Presets</a>. encontre o q mais se aproxima do q vc
          gosta e use, ou altere a seu gosto a partir de um desses.
        </p>
        <p class="text-base mb-4">Uma outra opção para personalizar o prompt é o <a class="link" href="https://github.com/ohmybash/oh-my-bash">Oh-My-Bash</a>, que pelo nome dá pra notar, é para uso no Bash, mas que tem versão para <a class="link" href="https://ohmyz.sh/">Zsh</a>, <a class="link" href="https://github.com/oh-my-fish/oh-my-fish">Fish</a> e até para <a class="link" href="https://ohmyposh.dev/">Power shell</a>, uma boa surpresa. São fáceis de instalar e configurar, a parte da personalização é bem simples e o tempo q leva só depende do quão longe se quer ir das opções padrão e por qual caminho (editando um arquivo pronto q mais se aproxima do desejado ou começando do zero depois de entender como alterar os parâmetros dos arquivos de configuração, os chamados dotfiles).</p>
        <h2 class="text-3xl mb-4 mt-8">O comando li</h2>
        <p class="text-base mb-2">O comando em si é um alias para:</p>
        <pre class="w-fit rounded-lg border-2 border-slate-800 transition-all duration-500 mb-2 py-2 px-4 bg-slate-500">'exa -lah --icons'</pre>
        <p class="text-base mb-4">O comando <a class="link" href="https://the.exa.website/">exa</a>, como dito logo no início em seu site, se trata de um substituto moderno para o ls. Aceita as mesmas flags e tem algumas opções a mais.</p>
        <p class="text-base mb-4">Tenho usado há algum tempo e me sinto satisfeito com a mudança, uso com essas opções pq gosto das listagens longas (o 'l'), gosto de ver todos os arquivos (o 'a', de all), prefiro saber o tamanho dos arquivos em unidades mais fáceis de compreender (o 'h' de humano) e acho a exibição dos ícones (aqui é só do exa mesmo, o '--icons') na lista bem útil e tb mais bonita, pq ñ dizer, assim como o colorido da lista, q vc vai acostumando pra diferenciar certas coisas.</p>
        <h2 class="text-3xl mb-4 mt-8">Tmux</h2>
        <p class="text-base mb-4">
          O tmux é um pouco diferente, a customização q eu fiz depende da instalação de diversos plugins, e há várias
          formas de instalar cada um deles tb, assim como uma lista enorme para se escolher. Depois de procurar um
          pouco, descobri q a partir de um plugin, q basicamente serve para instalar e atualizar outros plugins, a
          tarefa seria bem mais leve do q inicialmente achava.
        </p>
        <p class="text-base mb-4">O plugin em questão é o <a class="link" href="https://github.com/tmux-plugins/tpm">Tmux Plugin Manager - TPM</a>, q mostra sua instalação, como instalar outros, exemplos e um <a class="link" href="https://github.com/tmux-plugins/list">link</a> com uma lista de plugins, com as mais variadas funcionalidades, para escolher, recomendo muito.</p>
      </Card>
      <Card>
        <template #titulo>Editores</template>
        <p class="text-base mb-4">Essa não é uma dica de interface, pelo menos não apenas de interface, uma vez que as alterações realizadas no editores não tem fim apenas estético (embora isso ajude muito tb), mas principalmente são uma forma de facilitar o uso, aumentar as funcionalidades e deixar a curva de aprendizado para uma produtividade razoável menos íngrime.</p>
        <h2 class="text-3xl mb-4">Neovide com AstroVim</h2>
        <p class="text-base mb-4">Uma escolha entre tantas, com o <a class="link" href="https://astronvim.com/">AstroVim</a> tanto as transformações na aparência qto novas funcionalidades já vem todas no mesmo pacote. Embora seja possível customizar além disso e haja temas para q a aparência assuma outras formas, à gosto do usuário, vc instala o pacote e tudo já está lá. tudo bem direto ao ponto</p>
        <h2 class="text-3xl mb-4">Spacemacs</h2>
        <p class="text-base mb-4">Não muito diferente do anterior em conceito, tb é um conjunto de 'ferramentas' (plugins, temas e extensões, aqui chamadas de layers) q preparam o <a class="link" href="https://www.spacemacs.org/">Emacs</a> para um uso mais parecido com editores de texto de interface gráfica, com muitas funcionalidades com acesso simplificado.</p>
        <h2 class="text-3xl mb-4">Vim customizado</h2>
        <p class="text-base mb-4">Para as alterações no Vim, q eu preferi não usar o mesmo dotfile do NeoVim (q por sua vez compartilha as configurações do Neovide, já citado e com uma imagem na página About), eu tive outra abordagem, mas não ficou sem sua cota de modificações.</p>
        <p class="text-base mb-4">As customizações são extensas e feitas 'à mão', uma a uma. Encontrei um vídeo com essas dicas e fui seguindo e alterando, não fiz exatamente como está no vídeo, uma vez q se trata de uma customização, então deve ficar como eu gostaria e ñ necessariamente como mostrado no vídeo.</p>
        <p class="text-base mb-4">O <a class="link" href="https://www.youtube.com/watch?v=hdZMqMeruSQ">vídeo</a> em questão é muito útil e merece uma conferida, ainda q ñ se vá fazer o q ele sugere, só pelo conhecimento q acaba sendo transmitido de qq forma. Como é muita coisa e tudo está bem explicado, não é um vídeo rápido, tem um pouco mais de 1h de duração, mas vale o tempo investido.</p>
      </Card>  
      <Card>
        <template #titulo>Gopher Hole</template>
        <p class="text-base mb-4">Levei um tempo para conseguir fazer funcionar, para descobrir o motivo de não funcionar e coisas do tipo, mas com a página funcionando, comecei a explorar o que o protocolo tem a oferecer. Ainda está bem no começo, mas espero já ter ferramentas o suficiente para dar andamento.</p>
        <h2 class="text-3xl mb-4">Minha 'toca' no Gopher</h2>
        <p class="text-base mb-4">Coloquei algumas imagens na página About com minha página inicial, usando o navegador de terminal Links (funciona de forma semelhante com o lynx, o Links e o Elinks) e outra imagem com o Lagrange, que tem uma interface mais parecida com navegadores web. Falo de navegadores web porque o protocolo Gopher é anterior ao protocolo http da web e funciona de forma um tanto diferente e continua servindo aos mesmos propósitos da época em que foi inicialmente projetado, servir textos, links e arquivos, sem execução de scripts (dá pra executar scripts, mas nada parecido com o que se faz com o Javascript).</p>
        <p class="text-base mb-4">Para criar a página em si usei as instruções na página do Github do <a class="link" href="https://github.com/gophernicus/gophernicus/blob/master/README.gophermap">Gophernicus</a>, onde há um arquivo de exemplo. Como achei que não seria suficiente, comecei a procurar por exemplos (achi muito mais do que esperava) e também ferramentas para automatizar o processo ou facilitar a criação de novas páginas (aí não achei tantas quanto esperava).</p>
        <p class="text-base mb-4">Testei umas 4 ou 5 diferentes, não funcionaram como eu esperava ou nem funcionaram, não tenho certeza de faltou alguma ação de minha parte ou permissão, mas acabei achando uma, chamada <a class="link" href="https://github.com/jamestomasino/burrow">Burrow</a>, com algumas variâncias, escolhi a que está no link e usei sem instalação mesmo. A ferramenta cria novas entradas de phlog, um nome alternativo para blog (blog é uma abreviação de weblog, phlog seria o mesmo para um gopher, assim como glog) de uma maneira bastante simples e automatizando boa parte das tarefas.</p>
        <p class="text-base mb-4">Como dá para ver nas imagens da página About, o tipo de navegador usado também influencia muito na experiência. Para ver em navegadores mais tradicionais é necessário instalar extensões para que consigam renderizar o protocolo, que funciona de maneira relativamente diferente.</p>
        <p class="text-base mb-4">Se quiser conferir a página, procure a extensão para seu navegador (não gostei muito dos resultados, mas pelo menos carrega alguma coisa) ou use um navegador de terminal, ou instale o Lagrange e visite o seguinte endereço:</p>
        <pre class="w-fit rounded-lg border-2 border-slate-800 transition-all duration-500 mb-2 py-2 px-4 bg-slate-500">gopher://vaporhole.xyz/1/~teseu</pre>
        <p class="text-base mb-4">Nem deixei como link, porque normalmente nem funcionaria (eu tenho a extensão instalada, mas quase sempre não uso links, copio e abro em outro lugar), aí é só copiar e colar em outro navegador compatível.</p>
      </Card>
    </div>
  </div>
</template>
<style scoped>

</style>
