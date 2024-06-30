# Desafio de Projeto - Criando um Podcast com IAs Generativas

![Static Badge](https://img.shields.io/badge/Status_Projeto:-Concluído_(30/Jun/2024)-green)

![Static Badge](https://img.shields.io/badge/Inteligência_Artificial_(IA)-blue)
![Static Badge](https://img.shields.io/badge/IA_Generativa-blue)
![Static Badge](https://img.shields.io/badge/Edição_e_Conversão_de_Áudio-blue)

![Static Badge](https://img.shields.io/badge/ElevenLabs-orange)
![Static Badge](https://img.shields.io/badge/CapCut-orange)
![Static Badge](https://img.shields.io/badge/AudioJoiner-orange)
![Static Badge](https://img.shields.io/badge/OpenIA-orange)
![Static Badge](https://img.shields.io/badge/ChatGPT-orange)

<br>

## 📒 Descrição

Projeto realizado com o objetivo de criar um podcast tech utilizando inteligência artificial

<br>

## 💻 Tecnologias Utilizadas

- Para criar o roteiro, utilizei o [ChatGPT](https://chatgpt.com/)
- Para gerar os áudios, utilizei a [Elevenlabs](https://elevenlabs.io/)
- Para edição e conversão de áudio, utilizei as ferramentas [Audio Joiner](https://audio-joiner.com/), [CapCut](https://www.capcut.com/editor) e [FreeConverter](https://www.freeconvert.com/pt/mp4-to-mp3/)

<br>

## 🧠 Prompts e Desenvolvimento
O primeiro passo foi pensar em um tema para meu podcast. Como estou fascinado pelo mundo de programação low-code / no-code, resolvi abordar sobre isso, focando em novos desenvolvedores e em pessoas de outras áreas que desejam fazer migração para a área de TI.

Com isso em mente, pus a mão na massa para criar o prompt de roteiro. No ChatGPT, inseri escrevi o prompt abaixo:

~~~
Você é um roteirista de podcast e iremos criar, juntos, um podcast de tecnologia, focado em programação low-code / no-code.
O nome deste podcast será dado por você e o público alvo serão desenvolvedores júniors em início de carreira, além de pessoas
que não atuam em TI e gostariam de fazer uma transição para a carreira de desenvolvimento.

Este podcast deve obedecer ao seguinte formato de roteiro:

[Introdução]
[Curiosidade 1]
[Curiosidade 2]
[Finalização]

{REGRAS}
- Crie um nome impactante para o podcast
- No bloco [Introdução], faça uma introdução semelhante às utilizadas pelo canal Código Fonte TV, como se tivesse
  sido escrito pelo Gabriel Fróes e/ou Vanessa Weber (eu os admirio muito)
- No bloco [Curiosidade 1], traga uma curiosidade sobre os conceitos de programação low-code / no-code
- No bloco [Curiosidade 2], fale sobre as principais ferramentas de low-code / no-code do mercado
- No bloco [Finalização], realize uma despedida final marcante, terminada por 'Eu sou o João e esse é o nosso
  [Nome do Podcast que você criou] deste semana!'
- Utilize uma liguagem leve e descontraída, além de amigável, típica de podcasts
- Este podcast terá 4 apresentadores: Elis, João, Aline e Pedro
- O podcast dever ser curto e cada bloco conter, no máximo, 330 caracteres
- Nos blocos [Introdução], [Curiosidade 1], [Curiosidade 2], comece se apresentando, sendo um para cada apresentador.
  Ex: eu sou o Pedro...

{REGRAS NEGATIVAS}
-- Não use vocabulário chulo nem terminologia técnica
-- Não ultrapasse 5 minutos de duração
~~~

Como já era esperado, o retorno do ChatGPT foi extraordinário:

~~~
Nome do Podcast: "Código Fácil"

[Introdução]
Olá, *pessoal! Sejam bem-vindos ao "Código Fácil"! Eu sou a Elis, e hoje vamos mergulhar no universo da programação
low-code e no-code. Se você está iniciando na carreira de desenvolvedor ou pensando em migrar para a área de TI,
esse podcast é para você. Vamos lá?

[Curiosidade 1]
Oi, eu sou o Pedro! Você sabia que com low-code e no-code é possível criar aplicativos sem escrever código? Essas
ferramentas foram feitas para simplificar o desenvolvimento, permitindo que qualquer pessoa, mesmo sem conhecimento
técnico, possa criar soluções digitais incríveis.

[Curiosidade 2]
Oi, eu sou a Aline! Existem várias ferramentas populares de low-code e no-code no mercado. Entre as mais conhecidas
estão o Microsoft Power Apps, que ajuda a criar aplicativos empresariais rapidamente, e o Bubble, que permite criar
web apps sem código. Essas ferramentas estão transformando o desenvolvimento!

[Finalização]
E aí, pessoal! Sou o João e espero que tenham gostado do nosso bate-papo sobre low-code e no-code. Fiquem ligados
nos próximos episódios para mais sobre programação descomplicada. Esse foi nosso "Código Fácil" desta semana!
Até a próxima!
~~~

Perfeito!

Com o roteiro em mãos, parti para a gravação dos áudios.

Conforme orientação, utilizei a plataforma de IA ***[Elevenlabs](https://elevenlabs.io/)*** e me deparei com um problema: ela é paga. Porém ela permite gravar áudios de até 330 caracteres, motivo pelo qual limitei cada bloco a esta quantidade.

Assim, criei 4 áudios diferentes, sendo um para cada bloco do roteiro, tomando o cuidade de utilizar um tom de voz (masculino/feminino) de acordo com o apresentador. O resultado foram os áudios abaixo:

- [Introdução](output/Introducao.mp3)
- [Curiosidade 1](output/Curiosidade1.mp3)
- [Curiosidade 2](output/Curiosidade2.mp3)
- [Finalização](output/Finalizacao.mp3)

O próximo passou foi fazer a junção dos arquivos de áudio e, para isso, utilizei a ferramenta online ***[Audio Joiner](https://audio-joiner.com/)***, que é super simples e direta de utilizar. Como resultado, gerei o áudio [Completo](output/PodCastCompleto.mp3).

Mas ainda faltava um algo mais, tipo... um áudio de fundo! Para isso, editei o arquivo com outra ferramenta online fantástica, chamada ***[CapCut](https://www.capcut.com/editor)***. Ao final da edição, ela gerou um arquivo .mp4, que precisei converter para .mpe utilizando o conversor online ***[FreeConverter](https://www.freeconvert.com/pt/mp4-to-mp3/)***.

<br>

## 📚 Resultado Final

O resultado final é um podcast simples e direto, 100% gerado com IA e, principalmente, com a curadoria humana, que é essencial para as entregas utilizando estas novas metodologias incríveis.

O podcast completo pode ser consultado aqui: [Podcast 'Código Fácil' - Episódio 1](output/PodCastCompletoComFundoMusical.mp3)

Espero que gostem!!! Foi muito divertido aprender brincando com estas maravilhas que a IA proporciona!

<br>

## 🔗 Referências

Projeto Base (DIO): [Criando um Podcast com IAs Generativas](https://web.dio.me/project/criando-um-podcast-com-ias/learning/14404448-7f07-4145-aa33-7be543a13afe?back=/track/santander-2024-fundamentos-de-ia-para-devs&tab=undefined&moduleId=undefined)
