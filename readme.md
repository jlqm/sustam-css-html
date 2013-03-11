# Framework para desarrollo de front-end

Con este framework se pretende optimizar el tiempo de  desarrollo de los sitios web así como mantener una guía de estilos, cumpliendo con las mejores prácticas en el desarrollo de Front-end ( CSS / HTML ). Este documento está basado principalmente en la guía de estilo de [Github](https://github.com/styleguide/css "Guía de estilo").
<br />
<br />

## Guía de estilo de Código

* usar tabulación con 2 espacios
* poner espacio después de : en declaraciones de propiedades
* poner espacios antes de \{ en declaraciones de reglas
* usar colores hexadecimales #000 a menos que se use RGBA
* usar // para comentar bloques de código ( en vez de /\* \*/)
* usar la medida de px para tamaños de fuentes ( en vez de em ó % )

<pre><code>// Este es un buen ejemplo!
.styleguide-format {
	border: 1px solid #0f0;
	color: #000;
	background: rgba(0,0,0,0.5);
}</code>
</pre>

*	Cualquier @variable ó @mixin que sea usado en más de un archivo deberá ir en la parte de <mark>globals/</mark>. Otros deberán ir al principio del archivo donde sean usados.
*	Como regla, la especificidad de css no debe de tener mayor profundidad a 3 selectores.


### Organización de archivos

La organización de archivos esta dividida en carpetas, cada carpeta almacena un conjunto de estilos para un componente en específico.

<pre>
styles
├── components
│   ├── comments.less
│   └── listings.less
├── globals
│   ├── mixins.less
│   ├── responsive_helpers.less
│   ├── base.less
│   ├── variables.less
├── plugins
│   ├── jquery.fancybox-1.3.4.less
│   └── normalize.less
├── grids
│   ├── 960gs ├── 960_12_col.less
├── sections
│   ├── issues.less
│   ├── profile.less
└── shared
    ├── forms.less
    └── markdown.less
</pre>


#### - carpeta "components"

Almacena componentes del sitio web.

Ejemplo:

* comentarios.less
* listados.less
* botones.less

#### - carpeta "globals"

Almacena los estilos base, funciones de less, reset de css para todos los navegadores, archivo de variables, etc.

Ejemplo:

* mixins.less ( funciones de less )
* responsive_helpers.less ( contiene media queries predefinidos )
* base.less ( estilos predefinidos )
* variables.less ( variables donde se almacenan colores, tamaños, etc. )

#### - carpeta "plugins"

Almacena los archivos CSS de los plugins utilizados dentro del sitio web.

Ejemplo:

* jquery.fancybox-1.3.4.less ( lightbox de jquery )

#### - carpeta "grids"

Almacena el framework del grid utilizado para el diseño del sitio web. Se incluye por default el [framework 960](http://960.gs "framework 960 grid system")

<br />

#### - carpeta "sections"

Almacena las distintas secciones del sitio web.

Ejemplo:

* perfil.less
* home.less
* contacto.less
* productos.less


#### - carpeta "shared"

Almacena los componentes que se comparten a travez de toda la aplicación.

* header.less
* footer.less
* sidebar.less
* navigation.less


### Convención de nombres de clases

Usar el prefijo <mark>is-</mark> para las reglas de estado compartidas entre CSS y JS.

Ejemplo:

<pre><code>// Este es un buen ejemplo!
.nav.is-open {
	background: #fff;
}

.nav.is-closed {
	background: #000;
}
</code></pre>

#### Especificidad ( classes vs ids)

Elementos que aparecen solo una vez dentro de una página deberían de usar IDs, en otro caso, se usan clases. Cuando se este en duda, se usa una clase.





<br /><br /><br /><br /><br /><br />