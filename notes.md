# Anotações do Curso "WordPress"

Além do conteúdo abaixo, Ramiro Lobo também disponibiliza outras dicas em seu em seu [site](https://www.ramirolobo.com/).

* Ferramentas utilizadas:
	* [FileZilla](https://filezilla-project.org/) – Ferramenta de cliente FTP para transferir arquivos para o seu servidor.
	* [Putty](https://www.putty.org/) – Ferramenta de SSH para acesso remoto ao seu servidor.
	* [ColorZilla](https://www.colorzilla.com/pt-br/) – Ferramenta para capturar cores em sites. Muito útil para manter a identidade de um site.
	* [Fontface Ninja](https://fonts.ninja/) – Ferramenta para identificar fontes usadas em sites.
	* [CSS Peeper](https://csspeeper.com/) - Ferramenta que realiza a a captura de cores, identifica fontes, permite baixar as imagens de um site e permite "inspecionar" trechos do código frontend de uma página visitada. Essa ferramenta é uma alternativa ao ColorZilla e Fontface Ninja.
	* [Notepad ++](https://notepad-plus-plus.org/downloads/) – Editor de código bem leve e eficiente, incluindo um cliente FTP (NppFTP).
	* [XAMPP](https://www.apachefriends.org/pt_br/index.html) – Pacote que inclui o Apache + MySQL/ MariaDB, PHP e o PHPmyAdmin. Crie um servidor na sua própria casa.
	* [WordPress](https://wordpress.org/) - CMS. Opte por baixar do wordress.org

* Preparação e instalação:
	* É recomendado a criação de 2 e-mails para:
		* Evitar que seja considerado spam e com isso, bloqueie o IP do servidor, atualmente, provedores sérios enviam somente e-mails autenticados.
		* Ao utilizar o mesmo endereço contato@dominio.com.br, se cliente alterar a senha do e-mail, quebrará a senha do servidor.
	* Sendo assim, por exemplo:
		* contato@dominio.com.br será o e-mail profissional, utilizado normalmente pelo cliente para o envio e recebimento de e-mails da empresa.
		* site@dominio.com.br será configurado no servidor para o envio de e-mails/formulários/troca de senhas. Este e-mail não será visto ou acessado por ninguém. A senha desse e-mail não deve ser repassada ao cliente para que não seja alterada e fique diferente do servidor.
		* Ao utilizar um servidor local (testes), atentar-se para a configuração SMTP e do arquivo .user.ini do e-mail.
	* Após instalar o Notepad++, instale o plugin [NppFTP](https://ashkulz.github.io/NppFTP/).
	* Instalando o WordPress no próprio computador:
		* Após instalar o XAMPP e iniciar o Apache e MySQL. Acesse [//localhost/phpmyadmin/](//localhost/phpmyadmin/) e crie um banco de dados (Ex.: Nome: cursowordpress e Character set: latin2_general_ci) conforme a imagem abaixo ![db-configurations-2](/images/db-configurations-2.png).
		* Descompacte o instalador do WordPress, deixando apenas a pasta wordpress na pasta do servidor (C:\xampp\htdocs). Após isso, renomeie a pasta wordpress com o nome da página (Ex.: cursowordpress).
		* Para instalar o WordPress, acesse [http://localhost/cursowordpress/](http://localhost/cursowordpress/).
		* Preencha o nome do banco, nome de usuário, senha, servidor do banco de dados e Prefixo da tabela conforme a imagem abaixo ![db-configurations-1.png](/images/db-configurations-1.png).
			* O prefixo da tabela poderá ser modificado visando uma maior segurança.
		* Preencha Título do site, nome do usuário, senha e e-mail conforme a imagem abaixo ![site-configurations](/images/site-configurations.png).
		* A alteração do usuário de admin para um nome personalizado é recomendado, visando uma maior segurança.
		
	* Instalando o WordPress manualmente:
		* Após acessar o endereço FTP através do FileZilla, crie uma pasta (Ex.: cursowordpress) e copie o instalador do WordPress para essa pasta.
		* A ferramenta PuTTY possibilita descompactar arquivos diretamente no servidor ao invés de descompacta-los no computador e enviar "cada arquivo" para o servidor FTP. Para isso, conforme a imagem abaixo, basta informar o FTP (deixando a porta informada como está), a Saved Sessions (Ex.: CursoWordPress) (e clique em Save), selecioná-la e clicar em Open. No primeiro acesso será necessário aceitar a troca de chaves, clicando em Sim. ![putty-configurations](/images/putty-configurations.png)
		* Após isso, poderá realizar a descompactação de arquivos através de um terminal Linux.
		* Feito isso, por meio do FileZilla, vá até a pasta wordpress e a renomeie (Ex.: manual).
		* Para instalar o WordPress, acesse [site/cursowordpress/manual](site/cursowordpress/manual) (Ex.: [www.cursoemvideo.com/cursowordpress/manual](www.cursoemvideo.com/cursowordpress/manual)).
		* Preencha o Nome do banco, Nome de usuário, Senha, Servidor do banco de dados e Prefixo da tabela conforme a imagem em anexo.
			* O prefixo da tabela poderá ser modificado visando uma maior segurança.
		* Preencha Título do site, Nome do usuário, Senha e e-mail conforme a imagem abaixo ![site-configurations](/images/site-configurations.png).
		* A alteração do usuário de admin para um nome personalizado é recomendado, visando uma maior segurança.

* Instalando Temas e Plugins:
    * Plugins e temas não utilizados devem ser excluídos e não somente desativados visando segurança e otimização.
	* Tema pai não deverá ser ativado nunca porque quaisquer alterações no tema, serão implementadas no nosso site. Sendo assim, por questão de segurança, utiliza-se e ativa-se o tema filho.
	* Instale o plugin [Astra](https://wpastra.com/) e não o ative.
	* Acesse o site [child-theme-generator](https://wpastra.com/child-theme-generator/) e gere o tema filho, conforme a imagem abaixo ![astra-child-theme-generator](/images/astra-child-theme-generator.png). Feito isso, envie o tema gerado para o WordPress, conforme a imagem abaixo ![theme-configurations](/images/theme-configurations.png)
	* Exclua o plugin "Akismet Anti-Spam" e o "Hello Dolly"

	* Instale os seguintes plugins:
		![plugins](/images/plugins.png)

		* [Editor clássico](https://br.wordpress.org/plugins/classic-editor/) - Um editor mais simples, é utilizado para editores que não tem conhecimento ou familiaridade com o editor de blocos. Ao ativa-lo após a ativação do Spectra e do Microthemer, aparecerá uma mensagem de não funcionamento do mesmo. Clique em configurações, deixe o editor em blocos como padrão e permita que o usuário alterne entre os tipos de editores, conforme a imagem abaixo ![block-editor](/images/block-editor.png).
		* [Companion Auto Update](https://wordpress.org/plugins/companion-auto-update/) - Utilizado para atualizar o WordPress, Plugins e temas. Recomenda-se realizar no máximo, 3 atualizações por vez devido ao timeout do provedor.
		* [EWWW Image Optimizer](https://br.wordpress.org/plugins/ewww-image-optimizer/) - Utilizado para o tratamento e compressão de imagens.
		* [MonsterInsights](https://br.wordpress.org/plugins/google-analytics-for-wordpress/) – Google Analytics Dashboard for WordPress Website Stats Made Easy - Utilizado para inserir a tag do Google Analytics. Anteriormente se chamava Google Analytics for WordPress by Monsterinsights.
		* [Importador do WordPress](https://br.wordpress.org/plugins/wordpress-importer/) - Utilizado para importar páginas de outros sites.
		* [Imsanity](https://wordpress.org/plugins/imsanity/) - Utilizado para o tratamento e compressão de imagens. Obs.: Atualmente o EWWW Image Opimizer realiza o mesmo que Imsanity e ainda melhor, sendo assim poderá desativar e desinstalar o Imsanity.
		* [Microthemer](https://wordpress.org/plugins/microthemer/) - Editor visual de CSS. Com ele, é possível ver as alterações em tempo real .
		* [Rank Math SEO](https://br.wordpress.org/plugins/seo-by-rank-math/) - Ajuda a ter acesso às ferramentas de SEO necessárias para melhorar seu SEO e atrair mais tráfego para seu site.
		* [Really Simple SSL](https://wordpress.org/plugins/really-simple-ssl/) - Converte http para https. Recomenda-se o uso provisório até que a correção seja feita e o site seja criado já em https (com certificado digital) e/ou enquanto é realizada a migração de um provedor sem https para um que já o tenha. O uso provisório é recomendado porque exige um processamento a mais no site. É importante utiliza-lo porque o Google penaliza sites inseguros no seu ranqueamento. De maneira geral, o https consiste no http com criptografia de dados SSL.
		* [UpdraftPlus WordPress Backup Plugin](https://br.wordpress.org/plugins/updraftplus/) - Utilizado para realizar backup. Ele pode enviar esse backup para serviços de nuvem. É importante que o escolher um provedor que forneça backup e, além desse backup do provedor, realizar um segundo backup "pessoal" que possa ser acessado e/ou restaurado mais rapidamente. Anteriormente se chamava UpdraftPlus - Backup/Restore.
		* [WP Mail SMTP](https://wordpress.org/plugins/wp-mail-smtp/) - Facilite a entrega de e-mail para WordPress. Também não deve ser utilizado constantemente. Apenas para eventuais correções/migrações.
		* [WP Super Cache](https://br.wordpress.org/plugins/wp-super-cache/) - Utilizado para ajudar na performance/velocidade do site. É importante utiliza-lo porque o Google penaliza sites lentos no seu ranqueamento.
		* [WPForms Lite](https://br.wordpress.org/plugins/wpforms-lite/) - Utilizado para fazer formulários, uma vez que o WordPress não tem formulários nativamente. Conta com função arrastar/soltar.
		* [WPS Hide Login](https://br.wordpress.org/plugins/wps-hide-login/) - Modifica o caminho de login ([wp-admin](wp-admin) (http://localhost/cursowordpress/wp-admin/ ou https://www.cursowordpress/wp-admin/) e [wp-login.php](wp-login.php)).
		* [Spectra – WordPress Gutenberg Blocks](https://br.wordpress.org/plugins/ultimate-addons-for-gutenberg/) - Editor em blocos que anteriormente se chamava "Gutenberg Blocks - Ultimate Addons for Gutenberg". É uma alternativa a versão paga do "WordPress Page Builder - Beaver Buider", que é utilizado profissionalmente.

* Configurações Importantes:
	* Em configurações gerais:
		* Preencha o título do site, descrição, endereço do WordPress (URL), endereço do site (URL).
		* Atente-se para que o endereço do WordPress e do site estejam com HTTPS.
		* A opção de membros é utilizada somente para sites de lojas e membros se cadastrarem.
		* A função padrão para novo usuário varia de acordo com o nível de privilégio dele.
		* WPS Hide Login modifica wp-admin para um nome que eu queira. Também posso modificar a pagina para onde será redirecionado caso seja acessado o wp-admin.

	*	Em configurações de escrita:
		* É possível categorizar os padrões de post. Isso será feito a medida em que se criam novos posts.
		* Pode ser realizado publicações através de e-mails configurados. Sendo uma ótima opção para jornalistas, essa opção representa um pequeno risco de serem publicadas itens errados ou de conteúdo não pertencente ao site. Para evitar possíveis problemas, as publicações podem ser realizadas através do app do WordPress para dispositivos móveis.

	* Em configurações de leitura:
		* É possível escolher a página inicial como o post mais recente ou uma página estática (página inicial).
		* É possível alterar a quantidade máxima de posts exibido por páginas. Quanto maior o número, mais lento ficará a página.
		* É possível configurar o número de posts no feed RSS para agregadores de notícias.
		* É possível evitar que mecanismos de busca indexem o site através do controle.

	* Configuração de discussão:
		* Nessas configurações existem algumas opções interessantes, dependendo do tipo de site criado.
		* Desabilite a opção de me enviar um email quando alguém publicar um comentário.
		* Habilite a opção em que o comentário deve ser aprovado manualmente.
		* Habilite a classificação do conteúdo de acordo com a idade.

	* Configurações de mídia:
		* O WordPress criará três imagens (grande, médio e miniatura) de acordo com os tamanhos pré-definidos nesse campo. Os tamanhos das imagens são importantes para a performance do site.
		* Habilite a organização de arquivos enviados em pastas baseadas no mês e ano. Como o FTP lista no máximo 10000 arquivos, se desabilitado, poderá não ser possível "trazer" todos os arquivos.

	* Configurações de links permanentes
		* Opte por configurar como dia e nome (Ex.: http://localhost/cursowordpress/2022/09/09/post-exemplo/)

	* Configurações de plugins:
		* Caso esteja utilizando o Imsanity, configure-o como na imagem abaixo ![images-configurations](/images/images-configurations.png).
		* O WPS Hide Login modifica o caminho de longin (wp-admin (http://localhost/cursowordpress/wp-admin/ ou https://www.cursowordpress/wp-admin/) e wp-login.php) para "dificultar" tentativas de invasão para infectar a máquina com bots e transformá-la em zumbis e vender serviços de ataque DDoS na deep web ou roubar base de dados do site. Após realizar o login, ele permite utilizar o wp-admin.
		* Deixe todas as configurações do Spectras ativadas e tão somente se não for utilizar alguma, desative-a.

	* Painel de Controle do WordPress
		* É possível exibir/ocultar páginas e menus.
		* Local onde se realiza a atualização do WordPress, Plugins, Temas e Traduções.
		* Posts podem ser utilizados para notícias, dicas e conteúdo que você queira compartilhar. Eles são organizados em categorias e tags. Esses elementos (tags e categorias) ajudam na indexação de informações e páginas dentro do próprio site.
		* Através da aba de mídia, é possível realizar a organização, upload, edição e redimensionamento e otimização de imagens.
		* Na aba comentários é possível gerenciar os mesmos.
		* Na aba aparência é possível habilitar e reorganizar os widgets.
		* Na aba ferramentas é possível realizar a exportação, diagnóstico entre outras opções disponíveis.

	* Como definir a Paleta de Cores para um Site
		* Recomenda-se criar um documento de texto (Google Docs ou Microsoft Word, por exemplo), conforme a imagem abaixo, com a proposta do site, contendo uma tabela das cores (cor e código hexadecimal) com a cor principal no centro, para "discutir" a proposta com o cliente. ![site-design-chooses](/images/site-design-chooses.png)
		* Sempre confira o código hexadecimal da cor com a ferramenta ColorZilla, uma vez que o preto pode não ser necessariamente 0,0,0.
		* [Colour Loves](https://www.colourlovers.com/) poderá ser utilizado para "inspiração" de cores quando não se tem nada ainda.
		* [Color Adobe](https://color.adobe.com/) ou [Coolors](https://coolors.co/) são utilizados para gerar a paleta de cores de acordo com uma determinada cor. Assim como no documento de texto, insira a cor principal no centro.
		* Não será utilizado todas as cores da paleta, necessariamente, assim como um fundo pode ser a cor com menor saturação, por exemplo.
		* Recomenda-se utilizar no máximo cores no site

	* Como escolher Fontes para um Site
		* No mesmo documento de texto citado acima, com a proposta do site, contendo uma tabela das cores (cor e código hexadecimal) deverá ser informado as fontes e qual o seu uso (título, destaques e conteúdo), conforme a imagem acima.
		* [Fonts Google](https://fonts.google.com/) é uma biblioteca de fontes, focado principalmente para web.
		* Recomenda-se utilizar 2 ou 3 fontes no site.
		* Fontes "serifa" são aquelas com um "traço" em cima e em baixo, sendo recomendada para papel (impresso) enquanto as outras são indicadas para telas (digital).

	* Dicas para Imagens em Site
		* Tecnicamente, você não deve utilizar imagens do Google Imagens devido aos direitos autorais, de uso, etc. Sendo assim, recomenda-se o uso de bancos de imagens como [Stock Adobe](https://stock.adobe.com) (pago), [Pexels](https://www.pexels.com/) (gratuito), [Pixabay](https://pixabay.com/) (gratuito) ou [Unplash](https://unsplash.com/) (gratuito).
		* Em relação ao tamanho da imagem, é recomendado o tamanho máximo de 1280 x 853 para destaques e tamanhos menores para outros usos.
		* Recomenda-se também, através de um editor de imagens, recortar a imagem no tamanho necessário e exporta-la com a compressão (qualidade) adequada para web (recomenda-se 72%).

	* HTML básico para WordPress
		* [Documentação HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
		* Títulos - a hierarquia de títulos vai de 1 a 6: <h1> </h1>
		* Parágrafo: <p> </p>
		* Negrito: <strong> </strong>
		* Itálico: <em> </em>
		* Quebra de linha: <br> ou <br />
		* Span - utilizado para configurar parte de um texto. Por exemplo: Preço: <span style="font-size: 1,8em; color: #144478">99</span>,90 onde span (<span> </span>) é o (style="font-size: 1.8em; color: #144478">99) são parâmetros. O 1.8em multiplica o tamanho da fonte 1.8x, sendo interessante pois este aumentará automaticamente ao aumentar o tamanho padrão da fonte do parágrafo. "font-size: 1.8em; color: #144478" é CSS.
			* &nbsp; - Espaço
			* #ffffff - Cor branca (ff é o maior número que pode ser representando em hexadecimal)
			* #000000 - Cor preta (00 de R, 00 de G e 00 de B)
			* <i class="fas fa-home"></i> - Ícone. No site [Fontawesome](https://fontawesome.com/) é possível pesquisar por ícones e copiar o código do mesmo.

	* Menus no WordPress
		* Aparência > Menus
			* Na página de menus no painel, há diversas configurações que podem ser feitas de acordo com a necessidade.
			* Configure links externos para abrir em novas abas para não retirar o usuário do acesso ao seu site.

	* Topo e Rodapé
		* Aparência > Personalizar
			* Insira a logo pequena no menu identidade do site. Recomenda-se modificar o título, texto alternativo e descrição da imagem para auxiliar na indexação, conforme a imagem abaixo ![images-acessibility](/images/images-acessibility.png).
			* Largura da logo: 132px
			* A customização do layout está disponível apenas na versão premium do Astra. Sendo assim, algumas configurações não serão possíveis de realizar algumas alterações no cabeçalho.
			* O caminho de navegação não foi utilizado, mas é importante para ranqueamento SEO.
			* A barra lateral é mais indicada para blogs apenas.
			* O trecho de código HTML "Curso em Vídeo [copyright] [current_year] [site_title] | Criado por <a href="https://portal.objetivonhn.com.br" target="_blank">Diego Roque</a>" (sem as aspas externas) não funcionou no menu de edição do rodapé. Todavia, é possível realizar edições através das ferramentas na própria página.
			* Container é a "caixa" contendo a informação do site entre as "margens" da tela (idem um documento de Word).
			* Os containers podem ser editados em diferentes projetos. Todavia, recomenda-se que os containers sejam iguais entre si em todas as páginas. Se não for realizadas alterações, pode deixar 1200px como padrão.
			* Cores, tipografias e página inicial são configurados nos seus respectivos menus de edição.

	* Destaques do Site
		* Padding - dentro do elemento
		* Margem - fora do elemento
		* Não foi possível adicionar seções conforme a vídeo-aula devido à mudanças no Spectra.

	* Colunas e Caixas
	* Seção de Cardápio
