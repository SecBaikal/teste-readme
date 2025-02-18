  <h2>Versões Utilizadas no Projeto</h2>

<h3>1. Ruby</h3>
<p>O Ruby é uma linguagem de programação dinâmica, de alto nível e orientada a objetos, amplamente utilizada para o desenvolvimento de aplicações web. No projeto, estamos utilizando a versão 2.7.2 do Ruby.</p>

<h3>2. RVM (Ruby Version Manager)</h3>
<p>O RVM é uma ferramenta poderosa para gerenciar várias versões do Ruby em seu sistema. Ele permite que você instale e altere versões do Ruby de forma simples, além de gerenciar as gemas (dependências) de maneira eficiente.</p>
<p><strong>Versão do RVM:</strong> <em>1.29.12</em> (última versão estável).</p>

<h3>3. Rails</h3>
<p>O Rails é um framework de desenvolvimento web escrito em Ruby, que segue o padrão de arquitetura MVC (Model-View-Controller). Este projeto está utilizando o Rails versão 6.1.3.</p>

<h2>Documentação de Instalação do RVM, Ruby e Rails</h2>

<h2>1. Remover a RVM</h2>
<p>Para remover a RVM do seu sistema, execute o seguinte comando:</p>
<pre><code>rvm implode</code></pre>

<h3>1.1. Limpar arquivos relacionados ao RVM</h3>
<p>Abra os seguintes arquivos no Visual Studio Code:</p>
<pre><code>code .zshrc</code></pre>
<pre><code>code .zlogin</code></pre>
<pre><code>code .bashrc</code></pre>
<pre><code>code .bash_profile</code></pre>
<pre><code>code .profile</code></pre>
<p>Use o comando <strong>CTRL + H</strong> para pesquisar e apagar tudo relacionado ao RVM nesses arquivos.</p>

<h2>2. Instalar o RVM</h2>
<p>Para verificar se o RVM ainda está instalado, use:</p>
<pre><code>rvm -v</code></pre>

<p>Se tudo relacionado ao RVM foi removido, instale as dependências necessárias:</p>
<pre><code>gpg2 --keyserver keyserver.ubuntu.com --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB</code></pre>

<p>Agora, instale o RVM:</p>
<pre><code>curl -sSL https://get.rvm.io | bash -s stable</code></pre>

<p>Carregue o RVM com o seguinte comando:</p>
<pre><code>source /home/"nome do seu usuario"/.rvm/scripts/rvm</code></pre>

<p>Para instalar os arquivos do shell automaticamente:</p>
<pre><code>curl -sSL https://get.rvm.io | bash -s stable --auto-dotfiles</code></pre>

<p>Verifique se tudo foi instalado corretamente:</p>
<pre><code>rvm --version</code></pre>

<h2>3. Instalação do Ruby</h2>
<p>Abra o projeto e, no terminal, use o seguinte código para baixar a versão correta do Ruby:</p>
<pre><code>rvm install "ruby-2.7.2"</code></pre>

<p>Se necessário, force a instalação:</p>
<pre><code>rvm install "ruby-2.7.2" --force</code></pre>

<p>Verifique o log de instalação do Bundler:</p>
<pre><code>cat /home/arthur/.rvm/log/1738848831_ruby-2.7.2/gem.install.bundler.log</code></pre>

<p>Instale a versão correta do Bundler:</p>
<pre><code>gem install bundler -v 2.4.22</code></pre>

<h2>4. Gerar Documentação RI</h2>
<p>Para gerar a documentação Ruby Index (RI) para as versões do Ruby instaladas via RVM:</p>
<pre><code>rvm docs generate-ri</code></pre>

<h2>5. Comandos Gerais</h2>

<h3>5.1. Verificar versão do Ruby</h3>
<pre><code>ruby --version</code></pre>

<h3>5.2. Exibir versão do Bundler</h3>
<pre><code>bundle --version</code></pre>

<h3>5.3. Forçar a instalação do Ruby</h3>
<pre><code>rvm install "ruby-2.7.2" --force</code></pre>

<h3>5.4. Verificar o Bundler</h3>
<pre><code>bundle --version</code></pre>

<h3>5.5. Remover o Bundler do sistema</h3>
<pre><code>gem uninstall bundle</code></pre>

<h3>5.6. Reinstalar o Bundler</h3>
<pre><code>gem install bundler -v 2.4.22</code></pre>

<h3>5.7. Confirmar instalação do Bundler</h3>
<pre><code>bundle --version</code></pre>

<h3>5.8. Exibir versões do Ruby instaladas</h3>
<pre><code>rvm list</code></pre>

<h3>5.9. Verificar versão do RubyGems</h3>
<pre><code>gem -v</code></pre>

<h3>5.10. Atualizar RubyGems</h3>
<pre><code>gem update --system 3.1.4</code></pre>

<h3>5.11. Verificar funcionamento do Bundler após atualização</h3>
<pre><code>bundle --version</code></pre>

<h3>5.12. Instalar dependências do Gemfile</h3>
<pre><code>bundle install</code></pre>

<h3>5.13. Instalar gem nio4r</h3>
<pre><code>gem install nio4r -v '2.5.8' --source 'https://rubygems.org/'</code></pre>

<h3>5.14. Verificar portas abertas</h3>
<pre><code>sudo fuser 5432/tcp</code></pre>

<h3>5.15. Matar processo de porta</h3>
<pre><code>sudo kill 1090</code></pre>

<h3>5.16. Criar e migrar banco de dados do Rails</h3>
<pre><code>rails db:create</code></pre>
<pre><code>rails db:migrate</code></pre>

<h3>5.17. Rodar o servidor Rails</h3>
<pre><code>rails s</code></pre>

<h2>6. Login no Front</h2>
<p>Para acessar o console do Rails, use o comando:</p>
<pre><code>rails console</code></pre>

<h3>6.1. Criar um novo usuário</h3>
<pre><code>user = User.new(email: 'seu_email@example.com', password: 'sua_senha_aqui')</code></pre>

<h3>6.2. Procurar um usuário</h3>
<pre><code>user = User.find_by(email: 'youruser@gmail.com.com')</code></pre>

<h3>6.3. Alterar senha do usuário</h3>
<pre><code>user.password = '10203040!'</code></pre>

<h3>6.4. Salvar o usuário</h3>
<pre><code>user.save!</code></pre>
