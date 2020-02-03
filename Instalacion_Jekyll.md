# Intalación de Jekyll

Vamos a intalar el generador de páginas estáticas Jekyll. Lo configuraremos lo básico y explicaremos como añadir un tema nuevo.

Para instalar Jekyll tenemos que asegurarnos de que tenemos instalados los paquetes de `ruby-full` y las `build-essential`.

###### Instalamos los paquetes necesarios
~~~
sudo apt install ruby-full
sudo apt install build-essential
~~~

Una vez instalado **Ruby**, que es el lenguaje que utiliza Jekyll y el paquete `build-essential` necesario procedemos a instalar Jekyll con el comando `gem` de Ruby.

###### Instalamos Jekyll
~~~
sudo gem install jekyll
    .
    .
    .
    Parsing documentation for jekyll-4.0.0
    Installing ri documentation for jekyll-4.0.0
    Done installing documentation for http_parser.rb, eventmachine, em-websocket, concurrent-ruby, i18n,    ffi, sassc, jekyll-sass-converter, rb-fsevent, rb-inotify, listen, jekyll-watch, kramdown,     kramdown-parser-gfm, liquid, mercenary, forwardable-extended, pathutil, rouge, safe_yaml,   unicode-display_width, terminal-table, jekyll after 31 seconds
    23 gems installed

sudo gem install jekyll bundler
    -------------------------------------------------------------------------------------
    Jekyll 4.0 comes with some major changes, notably:

      * Our `link` tag now comes with the `relative_url` filter incorporated into it.
        You should no longer prepend `{{ site.baseurl }}` to `{% link foo.md %}`
        For further details: https://github.com/jekyll/jekyll/pull/6727

      * Our `post_url` tag now comes with the `relative_url` filter incorporated into it.
        You shouldn't prepend `{{ site.baseurl }}` to `{% post_url 2019-03-27-hello %}`
        For further details: https://github.com/jekyll/jekyll/pull/7589

      * Support for deprecated configuration options has been removed. We will no longer
        output a warning and gracefully assign their values to the newer counterparts
        internally.
    -------------------------------------------------------------------------------------
    Successfully installed jekyll-4.0.0
    Parsing documentation for jekyll-4.0.0
    Done installing documentation for jekyll after 0 seconds
    Successfully installed bundler-2.1.4
    Parsing documentation for bundler-2.1.4
    Done installing documentation for bundler after 3 seconds
    2 gems installed
~~~

Una vez que tenemos instalado e Jekyll vamos a crear un nuevo proyecto, indicandole el nombre del mismo, en mi caso lo voy a llamar `Alejandro-MG`.

###### Creamos un nuevo proyecto
~~~
jekyll new Alejandro-MG
    Running bundle install in /home/vagrant/Alejandro-MG... 
      Bundler: Fetching gem metadata from https://rubygems.org/....
      Bundler: ...........
      Bundler: Fetching gem metadata from https://rubygems.org/..
      Bundler: Resolving dependencies...
      Bundler: Using public_suffix 4.0.3
      Bundler: Using addressable 2.7.0
      Bundler: Using bundler 2.1.4
      Bundler: Using colorator 1.1.0
      Bundler: Using concurrent-ruby 1.1.5
      Bundler: Using eventmachine 1.2.7
      Bundler: Using http_parser.rb 0.6.0
      Bundler: Using em-websocket 0.5.1
      Bundler: Using ffi 1.12.1
      Bundler: Using forwardable-extended 2.6.0
      Bundler: Using i18n 1.8.2
      Bundler: Using sassc 2.2.1
      Bundler: Using jekyll-sass-converter 2.0.1
      Bundler: Using rb-fsevent 0.10.3
      Bundler: Using rb-inotify 0.10.1
      Bundler: Using listen 3.2.1
      Bundler: Using jekyll-watch 2.2.1
      Bundler: Using kramdown 2.1.0
      Bundler: Using kramdown-parser-gfm 1.1.0
      Bundler: Using liquid 4.0.3
      Bundler: Using mercenary 0.3.6
      Bundler: Using pathutil 0.16.2
      Bundler: Using rouge 3.15.0
      Bundler: Using safe_yaml 1.0.5
      Bundler: Using unicode-display_width 1.6.1
      Bundler: Using terminal-table 1.8.0
      Bundler: Using jekyll 4.0.0
      Bundler: Fetching jekyll-feed 0.13.0
      Bundler: Installing jekyll-feed 0.13.0
      Bundler: Fetching jekyll-seo-tag 2.6.1
      Bundler: Installing jekyll-seo-tag 2.6.1
      Bundler: Fetching minima 2.5.1
      Bundler: Installing minima 2.5.1
      Bundler: Bundle complete! 6 Gemfile dependencies, 30 gems now installed.
      Bundler: Use `bundle info [gemname]` to see where a bundled gem is installed.Retrying dependency api  due to error (2/4): Bundler::HTTPError Network error while fetching https://index.rubygems.org/api/v1/   dependencies?gems=jekyll%2Cjekyll-feed%2Cminima%2Ctzinfo%2Ctzinfo-data%2Cwdm (execution expired)
      Bundler: Following files may not be writable, so sudo is needed:
      Bundler: /usr/local/bin
      Bundler: /var/lib/gems/2.5.0
      Bundler: /var/lib/gems/2.5.0/build_info
      Bundler: /var/lib/gems/2.5.0/cache
      Bundler: /var/lib/gems/2.5.0/doc
      Bundler: /var/lib/gems/2.5.0/extensions
      Bundler: /var/lib/gems/2.5.0/gems
      Bundler: /var/lib/gems/2.5.0/specifications
    New jekyll site installed in /home/vagrant/Alejandro-MG. 
~~~

Nos quedaría una estructura de directorios similar a la siguiente:
~~~
Alejandro-MG/
├── 404.html
├── about.markdown
├── _config.yml
├── Gemfile
├── Gemfile.lock
├── index.markdown
└── _posts
    └── 2020-02-03-welcome-to-jekyll.markdown

1 directory, 7 files
~~~

Ahora podemos ver nuestra página por defecto activando el servidor local con el comando `bundle exec jekyll serve`.

Ya tenemos Jekyll instalado y con el proyecto creado, ahora podemos configurarlo a nuestro gusto. Vamos a indicar los ficheros de configuración y los directorio importantes.

* **/_config.yml**: Es el fichero de configuración principal, donde le indicamos un monton de párametros de la generación de la página estática. Si quieres saber más, te recomiendo pichar [AQUÍ](https://jekyllrb.com/docs/configuration/).
* **/_posts/**: Es el directorio donde tenemos que añadir los ficheros Markdown donde 

> Descargamos de [AQUÍ](http://jekyllthemes.org/) el tema.

~~~
mv Soot-Spirits-master /home/vagrant/Alejandro-MG/
cd Soot-Spirits-master
bundle install
    .
    .
    .
    Using minima 2.5.1
    Using unicode-display_width 1.6.1
    Using terminal-table 1.8.0
    Fetching github-pages 204
    Installing github-pages 204
    Bundle complete! 1 Gemfile dependency, 85 gems now installed.
    Use `bundle info [gemname]` to see where a bundled gem is installed.
    Post-install message from html-pipeline:
    -------------------------------------------------
    Thank you for installing html-pipeline!
    You must bundle Filter gem dependencies.
    See html-pipeline README.md for more details.
    https://github.com/jch/html-pipeline#dependencies
    -------------------------------------------------
~~~


Error de nokogiri:
~~~
sudo apt-get install build-essential patch ruby-dev zlib1g-dev liblzma-dev
sudo gem install nokogiri
~~~

~~~
mv Soot-Spirits-master/* .
~~~

~~~
bundle exec jekyll serve
    Configuration file: /home/vagrant/Alejandro-MG/_config.yml
                Source: /home/vagrant/Alejandro-MG
           Destination: /home/vagrant/Alejandro-MG/_site
     Incremental build: disabled. Enable with --incremental
          Generating... 
                        done in 1.671 seconds.
     Auto-regeneration: enabled for '/home/vagrant/Alejandro-MG'
        Server address: http://127.0.0.1:4000
      Server running... press ctrl-c to stop.
~~~