# Git - GitHub
	
	Sistema de control de versiones (CVS) distribuido que fue creado por Linus Torvalds en 2005. 

	Su origen se remonta a la necesidad de gestionar el desarrollo del kernel de Linux de manera más eficiente. 

	Antes de Git, se utilizaban otros sistemas de control de versiones como CVS y Subversion, pero Linus y otros desarrolladores encontraron limitaciones en ellos, especialmente cuando se trataba de colaborar en proyectos de gran escala y distribuidos.


	El propósito principal de Git es permitir a los desarrolladores llevar un registro de los cambios en su código fuente, facilitando la colaboración entre equipos de desarrollo y permitiendo un flujo de trabajo más eficiente. 

	Algunas de las características clave de Git incluyen ramificación (branching), fusión (merging), seguimiento de cambios (tracking changes), y la capacidad de trabajar de forma distribuida, lo que significa que cada desarrollador tiene una copia completa del repositorio en su propia máquina.

	
	En la actualidad, Git es ampliamente utilizado en la industria del desarrollo de software y en proyectos de código abierto en todo el mundo. 

	Es la columna vertebral de plataformas como GitHub, GitLab y Bitbucket, que proporcionan servicios para alojar repositorios Git en la nube y facilitar la colaboración entre desarrolladores. 

	Git ha demostrado ser una herramienta invaluable para gestionar el flujo de trabajo de desarrollo de software, desde proyectos pequeños hasta grandes empresas con equipos distribuidos globalmente. 

	Además, su flexibilidad y potencia lo hacen adecuado para una amplia gama de casos de uso más allá del desarrollo de software, como la escritura colaborativa y la gestión de archivos de configuración.



|| Versiones
	
	Git 1.0 (29 de diciembre de 2005):

		Esta fue la primera versión estable de Git, lanzada por Linus Torvalds. 

		Aunque era funcional, carecía de muchas de las características y comandos que ahora asociamos con Git.


	Git 1.5 (20 de junio de 2007):

		Esta versión trajo varias mejoras significativas, incluyendo mejoras en la gestión de ramas y etiquetas, así como la introducción del comando "git-svn" para interactuar con repositorios SVN.


	Git 1.7 (4 de mayo de 2010):

		Introdujo características como "git bisect" para ayudar a encontrar commits problemáticos, mejoras en la interfaz de usuario y en la gestión de submódulos.


	Git 2.0 (23 de mayo de 2014): 

		Esta versión trajo cambios importantes en la compatibilidad y en la interfaz de usuario, pero sin cambios drásticos en la funcionalidad principal de Git.


	Git 2.8 (29 de marzo de 2016):

		Introdujo el subcomando "git add -p" para una adición interactiva de cambios, mejoras en la velocidad y en la compatibilidad con Windows.


	Git 2.13 (30 de mayo de 2017):

		Introdujo una nueva opción "--no-edit" para "git rebase" y mejoras en el manejo de rebase interactivo.


	Git 2.20 (24 de diciembre de 2018): 

		Introdujo mejoras en la eficiencia y en el rendimiento, así como la opción de "git switch" para cambiar de rama de forma más segura.



|| Características
	
    Distribuido: 

    	Git es un sistema de control de versiones distribuido, lo que significa que cada desarrollador tiene una copia completa del repositorio en su propia máquina. 

    	Esto permite un flujo de trabajo descentralizado y una mayor resiliencia frente a fallos en comparación con los sistemas centralizados.


    Ramificación y fusión (Branching and Merging): 

    	Git facilita la creación de ramas (branching), lo que permite a los desarrolladores trabajar en diferentes características de forma simultánea sin interferir en el trabajo de los demás. 

    	La fusión (merging) permite combinar cambios de diferentes ramas de manera eficiente.


    Seguimiento de cambios (Tracking Changes): 

    	Git registra cada cambio realizado en el repositorio, lo que permite a los desarrolladores revisar el historial de cambios, revertir a versiones anteriores y entender cómo ha evolucionado el código con el tiempo.


    Eficiencia: 

    	Git está diseñado para ser rápido y eficiente, incluso en proyectos con un gran número de archivos y commits.

    	Utiliza algoritmos inteligentes para minimizar el tamaño de los repositorios y optimizar operaciones como la fusión y la recuperación de datos.


    Compatibilidad: 

    	Git es compatible con una amplia gama de sistemas operativos, incluyendo Linux, macOS y Windows.

    	También es compatible con múltiples protocolos de red, lo que permite a los desarrolladores acceder a repositorios remotos a través de HTTP, SSH, y otros protocolos.


    Herramientas de colaboración:

    	Git facilita la colaboración entre desarrolladores al proporcionar herramientas para compartir código, revisar cambios y resolver conflictos de manera eficiente.

    	Plataformas como GitHub, GitLab y Bitbucket ofrecen características adicionales para facilitar la colaboración en proyectos de código abierto y privados.


    Flexibilidad: 

    	Git es altamente configurable y se puede adaptar a una amplia variedad de flujos de trabajo y necesidades de desarrollo. 

    	Los desarrolladores pueden personalizar la configuración de Git y utilizar complementos y herramientas de terceros para ampliar su funcionalidad.	



|| Ejecutar Git
	
	Configuración inicial:

		Es buena práctica configurar tu nombre de usuario y tu dirección de correo electrónico. 



|| Config

	Forma en que se almacenan y gestionan las preferencias y ajustes del usuario. 

	Estos ajustes pueden ser globales (a nivel de usuario) o específicos de un repositorio. 

	La configuración de Git es muy versátil y te permite personalizar diversos aspectos del comportamiento de Git, como tu nombre de usuario, dirección de correo electrónico, alias, comportamiento de fusiones, y mucho más.


	Configuración global: 	

		se aplica a todos los repositorios de Git en tu sistema. 

		Utilizando: 

			config --global.		


		```
		git config --global user.name "Tu Nombre"
		git config --global user.email "tu@email.com"

		```


	Configuración Específica de Repositorio:

		Se aplica solo al repositorio actual en el que te encuentras. 

		Sin utilizar: 

			--global

		```
		git config user.name "Tu Nombre"
		git config user.email "tu@email.com"

		```


	Ver configuración: 	

		Configuración actual:

			git config --list	



	Editar configuración en Archivo: 

		Directamente en el archivo .git/config en el directorio raíz de tu repositorio.


	Alias: 	

		```	
		git config --global alias.co "checkout"
		git config --global alias.br "branch"

		```


	Comportamiento de Merge/fusiones: 	
		Cómo Git realiza y resuelve las fusiones entre ramas.

		
		Herramienta de Fusión (merge.tool):

			Git puede utilizar diferentes herramientas para resolver conflictos de fusión de manera visual.		


		Estilo de Conflictos de Fusión (merge.conflictstyle):

			El estilo de conflictos de fusión dicta cómo se presentan los conflictos de fusión en los archivos durante el proceso de fusión. 

			Hay varias opciones disponibles, como "merge" (el predeterminado), "diff3" y "mergeinfo". Por ejemplo:

		```	
		git config --global merge.tool "meld"	
		git config --global merge.conflictstyle "diff3"


		```		


	Resolución Automática de Conflictos (merge.ff):

		La opción "ff" (fast-forward) permite o evita que Git realice fusiones "fast-forward" cuando sea posible. 

		Puedes habilitarlo o deshabilitarlo según tus preferencias.



|| Conceptos
	
	Repositorio (Repository):

	    Un repositorio Git es un lugar donde se almacena tu código y su historial de cambios.

	    Puede ser un repositorio local en tu máquina o un repositorio remoto alojado en un servicio como GitHub, GitLab o Bitbucket.


	Commit:

	    Un commit en Git es un punto en el tiempo que representa un conjunto de cambios en tu código.

	    Cada commit tiene un mensaje descriptivo que explica los cambios realizados.

	    Los commits forman el historial de cambios del repositorio y son fundamentales para rastrear el progreso del proyecto y revertir cambios si es necesario.


	Rama (Branch):

	    Una rama en Git es una línea independiente de desarrollo que permite trabajar en nuevas características, arreglos de errores o experimentos sin afectar la rama principal del proyecto (generalmente llamada 'master' o 'main').

	    Las ramas permiten a los desarrolladores trabajar de forma paralela y fusionar los cambios cuando estén listos.


	Fusión (Merge):

	    La fusión en Git es el proceso de combinar los cambios de una rama en otra.

	    Se utiliza principalmente para integrar el trabajo realizado en una rama de desarrollo (por ejemplo, una rama de función) de vuelta a la rama principal del proyecto.


	Clonar (Clone):

	    Clonar un repositorio Git significa crear una copia local de un repositorio remoto en tu máquina.

	    Esto te permite trabajar en el código y contribuir al proyecto sin modificar el repositorio original.


	Estado del archivo (File Status):

	    Git rastrea el estado de los archivos en tu proyecto, que pueden estar en uno de tres estados: modificados, preparados (staged) y confirmados (committed).

	    Los archivos modificados son aquellos que han sido cambiados desde el último commit.

	    Los archivos preparados son aquellos que han sido marcados para ser incluidos en el próximo commit.

	    Los archivos confirmados son aquellos que han sido guardados en el repositorio mediante un commit.


	Repositorio remoto (Remote Repository):

 		Es un repositorio alojado en un servidor remoto, como GitHub, GitLab o Bitbucket.

	    Los desarrolladores pueden colaborar en un proyecto clonando el repositorio remoto, realizando cambios y enviando (pushing) esos cambios de vuelta al servidor remoto.



|| Sintaxis básica

	1. Config inicial: 

		Configuración básica.

		```
		git config --global user.name "Tu Nombre"
		git config --global user.email "tu@email.com"

		```


	2. Iniciar un Repositorio:	

		Empezar a versionar un proyecto.

		Inicializar un repositorio Git en el directorio del proyecto.

		```
		git init

		```


	3. Añadir y Confirmar Cambios:

		Una vez que has realizado cambios en tu proyecto, debes añadirlos al área de preparación y luego confirmarlos.

		```
		git add <archivo(s)>
		git commit -m "Mensaje descriptivo del commit"

		```


	4. Ramas:

		Útiles para desarrollar funcionalidades de forma aislada.

		```
		git branch                   # Lista todas las ramas

		git branch <nombre-rama>     # Crea una nueva rama

		git checkout <nombre-rama>   # Cambia a una rama existente

		git merge <nombre-rama>      # Fusiona cambios de una rama en la rama actual

		```


	5. Repositorios Remotos:

		Permiten colaborar con otros desarrolladores y respaldar tu código en la nube.

		```
		git remote add origin <URL>  # Añade un repositorio remoto
		
		git push -u origin <rama>    # Envía cambios al repositorio remoto
		
		git pull origin <rama>       # Obtiene cambios del repositorio remoto

		```


	6. Comandos específicos para el flujo de trabajo: 

		```
		git status                   # Muestra el estado actual del repositorio

		git log                      # Muestra el historial de commits

		git diff                     # Muestra las diferencias entre archivos

		git checkout -- <archivo>    # Descarta los cambios locales en un archivo

		git stash                    # Guarda temporalmente cambios no comprometidos

		```



|| Buenas prácticas

	Utiliza Ramas:

	    Crea ramas para cada nueva funcionalidad o tarea que vayas a desarrollar.

	    Mantén la rama master o main estable y lista para desplegar en producción.

	    Fusiona ramas solo cuando estés seguro de que los cambios funcionan como se espera.


	Escribe Mensajes de Commit Significativos:

	    Escribe mensajes de commit claros y descriptivos que expliquen qué cambios se realizaron y por qué.

	    Usa un formato consistente para tus mensajes de commit, como el formato imperativo ("Añade", "Corrige", "Actualiza", etc.).


	Realiza Commits Pequeños y Frecuentes:

	    Divide tus cambios en commits pequeños y coherentes en lugar de hacer un solo commit grande.

	    Realiza commits con frecuencia para capturar el progreso de tu trabajo y facilitar la revisión de cambios.


	Revisa y Comenta el Código:

	    Utiliza herramientas de revisión de código como GitHub, GitLab o Bitbucket para revisar los cambios de tus compañeros de equipo.

	    Comenta el código para explicar su funcionamiento, especialmente en áreas complejas o propensas a errores.


	Usa Ramas de Función y Pull Requests:

	    Utiliza ramas de función o feature branches para desarrollar nuevas características de forma aislada.

	    Crea pull requests o solicitudes de extracción para fusionar tus ramas de función en la rama master o main, y solicita la revisión de tus compañeros de equipo.


	Evita los Commits Directamente en master o main:

	    Evita realizar commits directamente en la rama master o main, especialmente en proyectos compartidos.

	    Utiliza ramas o branches de características para desarrollar y probar nuevas funcionalidades antes de fusionarlas en la rama principal.


	Realiza Pruebas Antes de Hacer Commit:

	    Asegúrate de que tu código pase todas las pruebas unitarias y de integración antes de hacer commit.

	    Utiliza herramientas de integración continua para automatizar las pruebas y garantizar la calidad del código.


	Mantén tu Repositorio Limpio:

	    Elimina ramas locales y remotas que ya no sean necesarias después de fusionar los cambios.

	    Utiliza herramientas como 'git clean' y 'git reset' para limpiar tu directorio de trabajo de archivos no rastreados y cambios no deseados.


	Documenta tu Proyecto:

	    Mantén un archivo 'README.md' que explique cómo instalar, configurar y utilizar tu proyecto.

	    Documenta las dependencias, los requisitos del sistema y cualquier información relevante para los colaboradores y usuarios.



|| Comandos
	
	Git tiene una amplia variedad de comandos para gestionar el control de versiones y el desarrollo de software. 

	Están disponibles a través de la línea de comandos de Git y pueden ser utilizadas para realizar diversas tareas relacionadas con el manejo de repositorios Git.

	
	Principales: 

		1. Inicializar un repositorio:
			
			'git init' permite crear un nuevo repositorio Git en un directorio específico.


	    2. Clonar un repositorio: 

	    	'git clone' permite crear una copia local de un repositorio Git remoto en tu máquina.


	    3. Agregar cambios al área de preparación: 

	    	'git add' permite agregar archivos modificados al área de preparación (staging area) para ser incluidos en el próximo commit.


	    4. Realizar un commit: 

	    	'git commit' permite crear un nuevo commit que registra los cambios realizados en el repositorio.


	    5. Crear y gestionar ramas: 

	    	'git branch' permite crear, listar y borrar ramas en el repositorio.

	    	'git checkout' permite cambiar entre ramas existentes.


	    6. Fusionar ramas: 

	    	'git merge' permite fusionar los cambios de una rama en otra.


	    7. Recuperar y revisar el historial de cambios: 

	    	'git log' permite revisar el historial de commits en el repositorio. 

	    	'git diff' permite ver las diferencias entre versiones de archivos.


	    8. Sincronizar cambios con repositorios remotos: 

	    	'git push' permite enviar cambios locales a un repositorio remoto. 

	    	'git pull' permite obtener cambios remotos y fusionarlos con el repositorio local.


	    9. Gestionar etiquetas: 

	    	'git tag' permite crear, listar y borrar etiquetas en el repositorio.


	    10. Resolver conflictos de fusión: 

	    	'git mergetool' y otras herramientas permiten resolver conflictos de fusión entre ramas.		


|| Lista de comandos
	
	Configuración y Estado del Repositorio:

	    git init: 

	    	Inicializa un nuevo repositorio Git.

	    git clone: 

	    	Clona un repositorio Git existente.

	    git status: 

	    	Muestra el estado actual del repositorio.

	    git config: 

	    	Configura opciones de Git, como nombre de usuario, correo electrónico, etc.

	    git log: 

	    	Muestra el historial de commits.

	    git diff: 

	    	Muestra las diferencias entre archivos.


	Gestión de Ramas:

	    git branch: 

	    	Lista, crea o elimina ramas.

	    git checkout: 

	    	Cambia entre ramas o versiones específicas.

	    git merge: 

	    	Fusiona cambios de una rama en otra.


	Trabajo con Commits:

	    git add: 

	    	Añade cambios al área de preparación.

	    git commit: 

	    	Crea un nuevo commit con los cambios del área de preparación.

	    git reset: 

	    	Deshace cambios en el área de preparación o en el directorio de trabajo.

	    git revert: 

	    	Crea un nuevo commit que revierte los cambios de un commit anterior.

	    git cherry-pick: 

	    	Aplica un commit específico a la rama actual.

	    git commit --amend: 

	    	Modifica el último commit.


	Gestión de Etiquetas:

	    git tag: 

	    	Crea, lista o elimina etiquetas.


	Trabajo con Repositorios Remotos:

	    git remote: 

	    	Administra conexiones a repositorios remotos.

	    git fetch: 

	    	Obtiene cambios de un repositorio remoto.

	    git pull: 

	    	Obtiene cambios de un repositorio remoto y los fusiona en la rama local.

	    git push: 

	    	Envía cambios locales a un repositorio remoto.


	Herramientas de Colaboración:

	    git merge --no-ff: 

	    	Realiza una fusión no rápida para preservar el historial de la rama.

	    git blame: 

	    	Muestra quién modificó cada línea de un archivo y en qué commit.

	    git bisect: 

	    	Ayuda a encontrar el commit que introdujo un error mediante búsqueda binaria.

	    git rebase: 

	    	Reordena, edita o combina commits en una rama.

	    git stash: 

	    	Guarda temporalmente cambios no comprometidos en una pila.


	Submódulos y Subárboles:

	    git submodule: 	

	    	Administra submódulos en el repositorio.

	    git subtree: 

	    	Permite trabajar con subárboles en Git.


	Otras Funciones Útiles:

	    git grep: 

	    	Busca cadenas de texto en archivos del repositorio.

	    git archive: 

	    	Crea un archivo comprimido de un árbol de trabajo o un commit.

	    git reflog: 

	    	Registra referencias de HEAD anteriores y ayuda a recuperar cambios perdidos.
	


|| Lista de banderas

	Banderas Globales:

	    --version: 

	    	Muestra la versión de Git instalada.

	    --help: 

	    	Muestra la página de ayuda para un comando específico.

	    --verbose o -v: 

	    	Proporciona información adicional en la salida.

	    --quiet o -q: 

	    	Suprime la salida normal, mostrando solo errores.

	    --dry-run:

	    	Ejecuta el comando en modo simulación, sin realizar cambios.


	Banderas para el comando git add:

	    --all o -A: 

	    	Añade todos los archivos, incluyendo los eliminados.

	    --patch o -p: 

	    	Interactivamente añade partes de los archivos.


	Banderas para el comando git commit:

	    --message o -m:

	    	Permite especificar un mensaje de commit en línea.

	    --amend: 

	    	Modifica el commit más reciente.


	Banderas para el comando git log:

	    --oneline: 

	    	Muestra cada commit en una sola línea.

	    --graph: 

	    	Muestra un gráfico ASCII de las ramas y fusiones.


	Banderas para el comando git branch:

	    --list o -l: 

	    	Lista todas las ramas.

	    --delete o -d: 

	    	Elimina una rama después de su fusión.


	Banderas para el comando git checkout:

	    --b: 

	    	Crea una nueva rama y se cambia a ella.

	    --track: 

	    	Configura una rama de seguimiento para la rama local.


	Banderas para el comando git merge:

	    --no-ff: 

	    	Realiza una fusión "no fast-forward".


	Banderas para el comando git remote:

	    --verbose o -v: 

	    	Muestra detalles verbosos sobre la configuración del control remoto.

	    --get-url: 

	    	Obtiene la URL de un control remoto.


	Banderas para el comando git push:

	    --force o -f: 

	    	Fuerza la actualización de referencias remotas.

	    --tags: 

	    	Envía etiquetas al control remoto.


	Banderas para el comando git pull:

	    --rebase: 

	    	Realiza un rebase en lugar de un merge.


	Banderas para el comando git stash:

	    --keep-index: 	

	    	Guarda solo los cambios que aún no han sido añadidos al área de preparación.

	    --include-untracked: 

	    	Incluye archivos no rastreados en el stash.


	Banderas para el comando git bisect:

	    --start: 

	    	Inicia una sesión de bisecting.


	Banderas para el comando git grep:

	    --count: 

	    	Muestra el número de líneas coincidentes.


	Otras Banderas Útiles:

	    --abbrev-commit: 

	    	Muestra un hash de commit abreviado.

	    --no-edit: 

	    	Utiliza el mensaje de commit predeterminado cuando se realiza una fusión o un rebase.



|| Crear repo

	Iniciar un nuevo repositorio Git en un directorio específico para comenzar a versionar y gestionar el código de un proyecto.

	```
	cd mi_proyecto
	git init

	```

	Añadir Archivos al Repositorio:

		Al área de preparación (staging area) utilizando el comando 'git add' para marca los archivos para ser incluidos en el próximo commit.

		```
		git add archivo1 archivo2 ...

		```


	Realizar commit: 

		Después de añadir los archivos al área de preparación, puedes crear el primer commit utilizando el comando 'git commit'.

		```
		git commit -m "Mensaje descriptivo del primer commit"

		```


	Repo remoto: 	

		Crear repositorios en servidores remotos como GitHub, GitLab o Bitbucket. 

		Permite respaldar tu código en la nube y colaborar con otros desarrolladores.

		Crea un nuevo repositorio vacío.

		Vincular tu repositorio local con el repositorio remoto.

		Enviar cambios locales al repositorio remoto.

		```
		git remote add
		git push

		```



|| Git Areas

	Donde se gestionan los cambios en los archivos de un proyecto.


	1. Directorio de Trabajo (Working Directory):

		Es el directorio en tu sistema de archivos donde estás trabajando en tus archivos de código. 

		Estos archivos no están bajo el control de Git hasta que se añaden al área de preparación.


	2. Área de Preparación (Staging Area):

		También conocida como "área de ensayo", es un área intermedia entre el directorio de trabajo y el repositorio Git. 

		Aquí es donde se preparan los cambios que se desean incluir en el próximo commit. 

		Los archivos que se añaden al área de preparación se seleccionan para ser parte del próximo commit.


	3. Repositorio Git (Git Repository):

		A veces llamado "área de confirmación", es donde se almacenan todos los commits y la historia de cambios del proyecto. 

		Una vez que los cambios se han confirmado (mediante un commit), quedan registrados de manera permanente en el repositorio.


	Flujo de Trabajo Básico:

		Implica mover cambios de un área a otra para prepararlos y confirmarlos.

	    Modificar Archivos: 

	    	Trabajas en tus archivos en el directorio de trabajo.


	    Añadir Cambios al Área de Preparación: 

	    	Utilizas el comando git add para añadir los cambios que deseas incluir en el próximo commit al área de preparación.


	    Confirmar Cambios al Repositorio: 

	    	Utilizas el comando git commit para confirmar los cambios en el área de preparación y registrarlos permanentemente en el repositorio Git.



|| Commit
	
	Son instantáneas de los cambios realizados en los archivos de un proyecto en un momento específico. 

	Cada commit tiene asociado un mensaje descriptivo que explica los cambios realizados. 

	Los commits son la base del control de versiones en Git y proporcionan un historial detallado de todos los cambios realizados en el proyecto a lo largo del tiempo.


	Identificador Único (SHA-1): 

		Cada commit en Git tiene un identificador único de 40 caracteres hexadecimal (SHA-1) que lo identifica de manera única en el repositorio.


	Mensaje Descriptivo: 

		Cada commit se acompaña de un mensaje descriptivo que explica los cambios realizados en ese commit. 

		Es importante proporcionar mensajes claros y concisos que expliquen el propósito y la razón de los cambios.


	Autor y Fecha: 

		Cada commit registra automáticamente el autor (nombre y dirección de correo electrónico) y la fecha en la que se realizó el commit.

	
	Padre(s): 

		Un commit puede tener uno o varios commits padre. 

		En la mayoría de los casos, un commit tiene un único commit padre, que es el commit anterior en la rama en la que se encuentra el commit. 

		Sin embargo, en casos de fusión (merge), un commit puede tener múltiples padres.


	Realizar commit: 

		Primero se deben añadir los cambios deseados al área de preparación utilizando el comando 'git add', y luego se ejecuta el comando 'git commit'.

		```
		git add archivo1 archivo2 ...  # Añade archivos al área de preparación
		git commit -m "Mensaje descriptivo del commit"  # Realiza el commit con un mensaje descriptivo

		```		


	Revertir commit: 

		Si es necesario deshacer un commit en Git, se pueden utilizar varios comandos, como 'git revert' para crear un nuevo commit que revierta los cambios realizados en un commit anterior, o 'git reset' para deshacer cambios y mover la rama a un commit anterior.

		Es importante tener en cuenta que estos comandos pueden afectar el historial de cambios del proyecto, por lo que se deben usar con precaución.



|| Sha1 Hash Objects

	Son identificadores únicos de 40 caracteres hexadecimales que se utilizan para representar y almacenar objetos, como archivos y commits, en el repositorio Git.

	SHA-1 (Secure Hash Algorithm 1) es un algoritmo criptográfico que genera un hash único para cualquier conjunto de datos de entrada.


	Características:

		Unicidad: 

			Cada objeto en Git, ya sea un archivo, un directorio o un commit, tiene un SHA-1 Hash único que lo identifica de manera única en el repositorio. 

			Esto permite que Git gestione eficientemente los objetos y garantiza la integridad de los datos.


		Integridad: 

			Los SHA-1 Hash se utilizan para verificar la integridad de los objetos en el repositorio Git. 

			Cualquier cambio en el contenido de un objeto resultará en un cambio en su SHA-1 Hash, lo que indica que el objeto ha sido modificado.


		Eficiencia: 

			Los SHA-1 Hash se utilizan para almacenar y recuperar objetos de manera eficiente en el repositorio Git. 

			Git utiliza el hash del contenido de los objetos como su identificador único, lo que facilita la búsqueda y recuperación de objetos durante las operaciones de control de versiones		


	Tipos de Objetos en Git:

	    Blob (Binary Large Object):

	    	Representa el contenido de un archivo en el repositorio. 

	    	Cada versión de un archivo se almacena como un objeto blob en Git.


	    Tree: 

	    	Representa la estructura de directorios en el repositorio Git. 

	    	Contiene referencias a los objetos blob y a otros objetos tree que representan los archivos y directorios del proyecto.


	    Commit: 

	    	Representa un conjunto de cambios realizados en el repositorio en un momento específico.

	    	Contiene referencias a un objeto tree que representa el estado del proyecto en ese momento, así como metadatos como el autor, la fecha y el mensaje del commit.


	Uso de los SHA-1 Hash Objects en Git:

	    Los SHA-1 Hash Objects se utilizan internamente por Git para almacenar y gestionar los objetos en el repositorio.

	    Los objetos se almacenan en el directorio '.git/objects' del repositorio Git, organizados en subdirectorios basados en los primeros caracteres del hash.

	    Los comandos de Git, como git add, git commit y git checkout, utilizan los SHA-1 Hash Objects para realizar operaciones de control de versiones en el repositorio.	


|| Modificar commit
	
	Realizar cambios en un commit existente o en el mensaje asociado a ese commit. 

	Aunque Git no permite modificar directamente un commit después de que se ha confirmado, existen algunas formas de realizar modificaciones a un commit, como corregir errores, ajustar el mensaje del commit o reorganizar los commits en la historia del proyecto.


	Modificar el Último Commit:

		Si quieres realizar cambios en el último commit que realizaste, puedes utilizar el comando 'git commit --amend'. 

		Este comando te permite agregar cambios adicionales al último commit, así como modificar su mensaje.

		```
		git add archivo_modificado
		git commit --amend

		```


	Reescribir el Historial de Commits:

		Si necesitas modificar commits anteriores en la historia del proyecto, puedes utilizar herramientas como 'git rebase' e 'interactive rebase'. 

		Con git rebase, puedes reorganizar, editar o eliminar commits en la historia de la rama actual.

		```
		git rebase -i HEAD~n
		
		```

		'n' es el número de commits que deseas revisar. 

		Esto abrirá un editor de texto interactivo donde puedes realizar las modificaciones deseadas.


	Deshacer Cambios en un Commit:

		Si necesitas deshacer cambios en un commit sin eliminar completamente el commit, puedes utilizar el comando 'git revert'. 

		Este comando crea un nuevo commit que revierte los cambios introducidos por un commit anterior.

		```
		git revert <hash_del_commit>

		```


	Modificar Mensajes de Commit Anteriores:

		Si necesitas modificar el mensaje de un commit anterior, puedes utilizar el comando 'git rebase' en modo interactivo para editar el mensaje del commit.

		```
		git rebase -i HEAD~n

		```

		Luego, cambia 'pick' por 'reword' en la línea correspondiente al commit cuyo mensaje deseas editar.

		Esto abrirá un editor de texto donde puedes modificar el mensaje del commit.



|| Undo commit 

	Proceso de deshacer un commit anterior realizado en el repositorio Git. 

	Hay varias formas de deshacer un commit en Git, dependiendo de si el commit que deseas deshacer es el commit más reciente o uno anterior en el historial del proyecto.


	Deshacer el Último Commit:

		Utilizar el comando 'git reset' con la opción --soft, --mixed o --hard, dependiendo de lo que desees hacer con los cambios realizados.

		
		1. Deshacer el Commit y Mantener los Cambios:

			Utiliza --soft. 

			Esto deshace el commit, pero deja los cambios realizados en los archivos sin confirmar.

			```
			git reset --soft HEAD~1

			```	


		2. Deshacer el Commit y Eliminar los Cambios del Área de Preparación: 

			Utiliza --mixed. 

			Esto deshace el commit y mueve los cambios realizados en el commit al directorio de trabajo, pero los deja sin confirmar.

			```
			git reset --mixed HEAD~1

			```


		3. Deshacer el Commit y Eliminar los Cambios:

			Utiliza --hard. 

			Esto deshace el commit y elimina los cambios realizados en el commit, restableciendo el proyecto al estado en el que estaba antes del commit.

			```
			git reset --hard HEAD~1

			```


	Deshacer Commit No Reciente: 

		Utilizar el comando 'git revert'. 

		Este comando crea un nuevo commit que revierte los cambios introducidos por un commit anterior.

		```
		git revert <hash_del_commit>

		```
		
		Proporcinar hash único del commit que deseas deshacer.


	Cuidados al Deshacer Commits:

    	Cuidado con el Historial Compartido: 

    		Si has compartido tu historial de commits con otros colaboradores, deshacer commits puede causar problemas si otros colaboradores ya han basado su trabajo en los commits que estás deshaciendo. 

    		En tales casos, es mejor considerar otras formas de corregir errores o realizar cambios en el proyecto.


	    Confirmación de Cambios: 

	    	Antes de deshacer un commit, asegúrate de guardar cualquier cambio importante que desees conservar. 

	    	El proceso de deshacer un commit puede eliminar permanentemente los cambios realizados en ese commit, así que asegúrate de revisar cuidadosamente qué cambios se van a deshacer.



|| Git Branches

	Línea independiente de desarrollo que representa una secuencia de commits. 

	Cada proyecto de Git puede tener múltiples ramas que funcionan de forma paralela, lo que permite a los desarrolladores trabajar en diferentes características, correcciones de errores o experimentos de forma aislada sin afectar la rama principal del proyecto.


	Características:	

		Rama Principal (Master o Main): 

			La rama principal, a menudo llamada "master" o "main", es la rama principal del proyecto y representa la versión estable y lista para producción del código.

			Todos los cambios importantes y estables se fusionan en esta rama.


		Ramas de Funcionalidad (Feature Branches): 

			Las ramas de funcionalidad son ramas temporales creadas para desarrollar nuevas características o funcionalidades. 

			Estas ramas se crean a partir de la rama principal y se eliminan después de que la funcionalidad se haya completado y fusionado de nuevo en la rama principal.


		Ramas de Corrección de Errores (Bug Fix Branches):

			Las ramas de corrección de errores se utilizan para corregir errores o bugs en el código. 

			Estas ramas se crean a partir de la rama principal y se fusionan de nuevo en la rama principal una vez que se han corregido los errores.


		Ramas de Versión (Release Branches): 

			Las ramas de versión se utilizan para preparar nuevas versiones del software para su lanzamiento. 

			Estas ramas se crean a partir de la rama principal y se utilizan para realizar pruebas finales y correcciones antes de la publicación de la versión.	


	Operaciones: 	

		Crear una Rama:

			Utiliza el comando 'git branch <nombre_rama>' para crear una nueva rama a partir de la rama actual.	

			```
			git branch nueva_rama

			```	


		Cambiar de Rama: 

			Utiliza el comando 'git checkout <nombre_rama>' para cambiar a una rama existente.

			```
			git checkout nombre_rama

			```


		Crear y Cambiar de Rama en un Solo Paso: 

			Utiliza el comando' git checkout -b <nombre_rama>' para crear una nueva rama y cambiar a ella en un solo paso.

			```
			git checkout -b nueva_rama

			```


		Eliminar una Rama: 

			Utiliza el comando 'git branch -d <nombre_rama>' para eliminar una rama después de que su trabajo se haya fusionado en otra rama.

			```
			git branch -d nombre_rama

			```


	Flujo de trabajo: 

		Implica crear ramas para desarrollar nuevas características o corregir errores, realizar commits en la rama correspondiente y luego fusionar los cambios en la rama principal cuando el trabajo esté completo.

		Esto permite un desarrollo paralelo y colaborativo mientras se mantiene la estabilidad del proyecto.



|| Git Push
	
	Comando para enviar los commits locales de tu repositorio a un repositorio remoto. 

	En esencia, se utiliza para sincronizar los cambios realizados en tu repositorio local con un repositorio remoto, como GitHub, GitLab o Bitbucket.


	Uso: 	

		Preparar Commits Locales:

			Antes de ejecutar git push, asegúrate de haber confirmado tus cambios localmente utilizando git commit.

			Los commits locales contienen los cambios que deseas enviar al repositorio remoto.


		Especificar el Repositorio Remoto: 	

			git push requiere que especifiques el repositorio remoto al que deseas enviar tus commits. 

			Por lo general, este repositorio se denomina origin de forma predeterminada, pero también puedes especificar un nombre diferente si es necesario.


		Enviar Commits al Repositorio Remoto: 	

			Una vez que hayas preparado tus commits locales y especificado el repositorio remoto, ejecuta el comando git push seguido del nombre de la rama que deseas enviar al repositorio remoto. 

			Por ejemplo, si deseas enviar la rama master:
	
			```
			git push origin master

			```

			Enviará los commits locales de la rama master al repositorio remoto llamado origin.


	Consideraciones: 

		Conflicto de Fusión: 

			Si otros desarrolladores han realizado cambios en el mismo archivo y rama en el repositorio remoto desde la última vez que hiciste 'git pull' o 'git fetch', podrías encontrar conflictos de fusión al intentar hacer 'git push'.

			En estos casos, deberás resolver los conflictos antes de poder enviar tus commits al repositorio remoto.

		
		Permisos de Escritura:

			Asegúrate de tener los permisos necesarios para hacer git push al repositorio remoto. 

			En algunos casos, es posible que necesites permisos de escritura para la rama específica a la que estás intentando hacer push.


				
|| Git Rebase

	Comando utilizado para reorganizar, combinar o modificar la historia de los commits en una rama. 

	A diferencia de 'git merge', que fusiona ramas conservando la historia original de los commits, 'git rebase' reescribe la historia de los commits para que parezca que los cambios fueron realizados en secuencia, una tras otra.

	
	Funcionamiento:

		1. Seleccionar una Rama Base:

			Para realizar un rebase, primero debes especificar la rama en la que deseas reorganizar la historia de los commits. 

			Esto se hace cambiando a la rama deseada utilizando 'git checkout' y luego ejecutando el comando git rebase seguido del nombre de la rama que deseas reorganizar.

			```
			git checkout tu_rama
			git rebase rama_base

			```

			Seleccionar la rama en la que deseas reorganizar la historia y ejecutar 'git rebase'.


		2. Reorganizar la Historia de los Commits: 

			Una vez que hayas ejecutado git rebase, Git intentará aplicar cada commit de 'tu_rama' uno por uno sobre la punta de la 'rama_base'.

			Si hay conflictos de fusión, Git pausará el proceso de rebase para que puedas resolverlos manualmente.


		3. Continuar o Detener el Rebase: 

			Después de resolver los conflictos de fusión, puedes continuar con el rebase utilizando 'git rebase --continue' o detenerlo utilizando 'git rebase --abort'.


	Uso: 

		Mantener un Historial de Commits Limpio: 

			'git rebase' se utiliza a menudo para mantener un historial de commits limpio y lineal, lo que facilita la lectura y la revisión del historial del proyecto.


		Integrar Cambios de una Rama a Otra: 

			También se utiliza para integrar cambios de una rama a otra, reorganizando la historia de los commits para que parezca que los cambios fueron realizados en secuencia.


		Simplificar la Historia del Proyecto: 

			En proyectos con muchos commits o ramas, 'git rebase' se puede utilizar para simplificar la historia del proyecto, fusionando commits relacionados o eliminando commits innecesarios.


	Consideraciones: 

		Reescribir la Historia del Proyecto: 

			Al utilizar 'git rebase', estás reescribiendo la historia de los commits en la rama seleccionada.

			Esto puede afectar a otros desarrolladores que estén trabajando en la misma rama, así que es importante comunicar cualquier rebase realizado a otros miembros del equipo.

		
		Potenciales Conflictos de Fusión: 

			Durante el rebase, es posible que encuentres conflictos de fusión que deban ser resueltos manualmente. 

			Estos conflictos pueden surgir cuando dos commits modifican el mismo archivo o línea de código.



|| Git Merge

	Fusionar los cambios de una rama en otra. 

	Permite combinar el trabajo realizado en diferentes ramas en un único punto, lo que facilita la integración de características, correcciones de errores o cualquier otro cambio en un proyecto.


	Funcionamiento: 

		1. Seleccionar la Rama Destino: 

			Antes de fusionar cambios, primero debes seleccionar la rama en la que deseas integrar los cambios. 

			Por lo general, esta es la rama en la que deseas aplicar los cambios realizados en otra rama

			Se utiliza 'git checkout'.

			```
			git checkout rama_destino

			```


		2. Ejecutar git merge:

			Una vez que estés en la rama destino, ejecuta el comando 'git merge' seguido del nombre de la rama que deseas fusionar en la rama destino.

			```	
			git merge rama_origen

			```

			Es la rama que contiene los cambios que deseas fusionar en la rama destino.


		3. Resolver Conflictos de Fusión (si es necesario): 

			Si Git detecta conflictos entre los cambios realizados en la rama origen y los cambios existentes en la rama destino, pausará el proceso de fusión y te pedirá que resuelvas los conflictos manualmente.

			Una vez resueltos los conflictos, puedes continuar con el proceso de fusión.


		4. Confirmar la Fusión:

			Después de resolver los conflictos de fusión (si los hubiera), Git creará un nuevo commit que fusiona los cambios de la 'rama origen' en la 'rama destino'. 

			Este commit de fusión registra la integración de los cambios y puede contener un mensaje de confirmación predeterminado o personalizado.


	Uso: 

		Integrar Funcionalidades:

			'git merge' se utiliza para integrar nuevas funcionalidades o características desarrolladas en una rama de características en la rama principal del proyecto.


	    Aplicar Correcciones de Errores: 

	    	También se utiliza para aplicar correcciones de errores o cambios de mantenimiento realizados en una rama de corrección de errores en la rama principal del proyecto.


	    Sincronizar Ramas: 

	    	Se utiliza para sincronizar los cambios realizados en diferentes ramas del proyecto, asegurando que todas las ramas estén actualizadas con los cambios más recientes.		


	Consideraciones: 	

		Potenciales Conflictos de Fusión: 

			Durante el proceso de fusión, es posible que encuentres conflictos si los cambios realizados en la 'rama origen' entran en conflicto con los cambios existentes en la 'rama destino'. 

			Estos conflictos deben ser resueltos manualmente antes de que la fusión pueda completarse.


    	Preservación del Historial de Commits: 

    		'git merge' crea un nuevo commit de fusión para registrar la integración de los cambios de la rama origen en la rama destino. 

    		Esto preserva el historial de commits y proporciona un registro claro de la fusión.


|| GitHub
	
	Plataforma de alojamiento de repositorios de código basada en la web que utiliza el sistema de control de versiones Git. 

	Permite a los desarrolladores almacenar y gestionar repositorios de Git de forma remota en servidores en la nube. 

	Los desarrolladores pueden crear repositorios públicos o privados en GitHub para alojar su código.


	Colaboración y Contribuciones:

		GitHub facilita la colaboración entre desarrolladores al permitirles clonar repositorios, realizar cambios locales y enviar solicitudes de extracción ('pull requests') para proponer cambios al código. 

		Esto es especialmente útil para proyectos de código abierto y equipos distribuidos.
		

	Seguimiento de Problemas y Solicitudes de Funcionalidades:

		Proporciona herramientas integradas para el seguimiento de problemas y solicitudes de funcionalidades ('issues'), lo que facilita la comunicación y la colaboración entre los miembros del equipo y los usuarios del proyecto.
	

	Integración con Herramientas de Desarrollo:

		Integra con una variedad de herramientas de desarrollo, como sistemas de integración continua ('CI'), herramientas de gestión de tareas y servicios de despliegue, lo que facilita la automatización de procesos y la gestión del ciclo de vida del desarrollo de software.


	Servicios:

		Además de alojar repositorios de código, GitHub ofrece una serie de servicios adicionales, como 'GitHub Pages' para alojar sitios web estáticos, 'GitHub Actions' para automatizar flujos de trabajo y 'GitHub Packages' para gestionar paquetes de software.
	


|| Pull Request
	
	Es una solicitud para fusionar los cambios realizados en una rama (generalmente una rama de características) en otra rama (generalmente la rama principal del proyecto, como "main" o "master").

	Facilita la colaboración y la revisión del código en proyectos alojados en plataformas como GitHub, GitLab o Bitbucket.


	Proceso: 

	1. Creación de una rama funcionalidad:

		El desarrollador trabaja en una nueva funcionalidad o una solución para un problema en una rama separada del repositorio. 

		Esto se hace generalmente creando una nueva rama a partir de la rama principal del repositorio.


	2.  Implementación de los Cambios:

		Realiza los cambios necesarios en la rama de características, agregando, modificando o eliminando código según sea necesario para implementar la funcionalidad o resolver el problema.


	3. Envío del Pull Request:

		Una vez que los cambios están listos para su revisión, el desarrollador crea un Pull Request desde su rama de características hacia la rama principal del repositorio. 

		Esto se hace típicamente a través de la interfaz web de la plataforma de alojamiento de código.
	

	4. Revisión del Código:

		Otros miembros del equipo o colaboradores revisan el código y los cambios propuestos en el Pull Request. 

		Pueden dejar comentarios, hacer preguntas o sugerir modificaciones antes de que los cambios se fusionen en la rama principal del repositorio.
	

	5. Discusión y Colaboración:

		El Pull Request se convierte en un lugar para discutir y colaborar en el código propuesto. 

		Los desarrolladores pueden responder a los comentarios, realizar cambios adicionales según sea necesario y trabajar juntos para mejorar la calidad del código.


	6. Fusionar el Pull Request:

		Una vez que los cambios han sido revisados y aprobados, un administrador del proyecto o un revisor autorizado puede fusionar el Pull Request en la rama principal del repositorio.

		Esto incorpora oficialmente los cambios propuestos en la rama principal y los hace parte del código base del proyecto.
		

	7. Cierre del Pull Request:

		Una vez que el Pull Request ha sido fusionado, se cierra oficialmente y se marca como completado en la plataforma de alojamiento de código.

		Esto ayuda a mantener un registro de los cambios realizados en el proyecto y proporciona transparencia sobre quién contribuyó con qué cambios y cuándo.



|| Remote Repo
	
	Repositorio alojado en un servidor remoto, como GitHub, GitLab o un servidor propio.

	Cuando trabajas con Git, generalmente tienes al menos un repositorio local en tu máquina, pero es común colaborar con otros desarrolladores y compartir tu trabajo en un repositorio remoto.


	1. Conexión con un Repositorio Remoto:

		Para conectar tu repositorio local a un repositorio remoto, puedes utilizar el comando 'git remote add'. 

		Esto establece una conexión entre tu repositorio local y el repositorio remoto, y te permite enviar y recibir cambios entre ellos.

		```
		git remote add nombre_remoto URL_repositorio_remoto

		```


	2. Listar Repositorios Remotos:

		Puedes ver una lista de los repositorios remotos asociados con tu repositorio local utilizando el comando git remote -v. 

		Esto te muestra los nombres y las URLs de los repositorios remotos.

		```
		git remote -v

		```


	3. Enviar Cambios al Repositorio Remoto:

		Cuando quieras enviar tus cambios locales al repositorio remoto, puedes utilizar el comando 'git push'. 

		Esto actualiza el repositorio remoto con tus cambios locales

		```
		git push nombre_remoto rama_local

		```


	4. Recibir Cambios del Repositorio Remoto:

		Cuando quieras obtener los cambios realizados en el repositorio remoto y aplicarlos a tu repositorio local, puedes utilizar el comando 'git pull'. 

		Esto descarga los cambios remotos y los fusiona automáticamente en tu rama local.

		```
		git pull nombre_remoto rama_remota

		```


	5. Clonar un Repositorio Remoto:

		Para crear una copia local de un repositorio remoto, puedes utilizar el comando 'git clone'. 

		Esto descarga todos los archivos y la historia del repositorio remoto y los coloca en un nuevo directorio en tu máquina.

		```
		git clone URL_repositorio_remoto

		```


	Consideraciones:

	    Los repositorios remotos son útiles para colaborar con otros desarrolladores y mantener una copia centralizada del proyecto.

	    Es importante tener cuidado al enviar cambios al repositorio remoto para evitar sobrescribir el trabajo de otros desarrolladores o perder cambios importantes.

	    La comunicación con el repositorio remoto a través de 'git push' y 'git pull' es esencial para mantener el proyecto actualizado y colaborar de manera efectiva con otros desarrolladores.



|| SSH Keys
	
	Una forma de autenticación que permite establecer conexiones seguras entre tu computadora y un servidor remoto.

	En el contexto de Git, las SSH keys se utilizan para autenticarse con servicios de alojamiento de repositorios remotos, como GitHub, GitLab o Bitbucket, sin tener que ingresar tu nombre de usuario y contraseña cada vez que interactúas con el servidor remoto.


	1. Funcionamiento las SSH Keys en Git:

	    Generación de Claves SSH:

	    	Primero, debes generar un par de claves SSH en tu computadora. 

	    	Este par consta de una clave pública y una clave privada.

	    	La clave pública se comparte con el servidor remoto, mientras que la clave privada se almacena de forma segura en tu computadora.


	    Asociación con tu Cuenta de Usuario: 

	    	Luego, asocias tu clave pública SSH con tu cuenta de usuario en el servicio de alojamiento del repositorio remoto.

	    	Esto le permite al servidor remoto reconocerte como un usuario autorizado cuando intentas acceder a tu repositorio.


	    Autenticación Automática:

	    	Cuando intentas realizar operaciones de Git que requieren autenticación, como clonar un repositorio o hacer push a un repositorio remoto, Git utiliza tu 'clave privada SSH' para autenticarte con el servidor remoto de forma automática y segura.


	2. Ventajas de Usar SSH Keys en Git:

	    Seguridad Mejorada: 

	    	Las SSH keys proporcionan una capa adicional de seguridad al evitar que tengas que ingresar tu nombre de usuario y contraseña en texto plano, lo que reduce el riesgo de que tus credenciales sean interceptadas.


	    Mayor Comodidad: 

	    	Una vez que has configurado tus SSH keys, puedes interactuar con los repositorios remotos de Git sin tener que ingresar tus credenciales cada vez.

	    	Esto simplifica el proceso y hace que sea más rápido trabajar con Git.


	    Autenticación de Dos Factores: 

	    	Algunos servicios de alojamiento de repositorios remotos, como GitHub, permiten configurar la autenticación de dos factores (2FA) con SSH keys, lo que proporciona una capa adicional de seguridad.


	3. Generación y Configuración de SSH Keys:

		La generación y configuración de SSH keys varían según el sistema operativo y el servicio de alojamiento del repositorio remoto. 

		Por lo general, puedes encontrar instrucciones detalladas en la documentación del servicio que estás utilizando. 

	    1. Generar un par de claves SSH en tu computadora.

	    2. Asociar tu clave pública SSH con tu cuenta de usuario en el servicio de alojamiento del repositorio remoto.

	    3. Configurar Git para que utilice tus SSH keys para autenticación.


	Es importante proteger tu clave privada SSH y no compartirla con nadie más. 

	Debes asegurarte de almacenarla en un lugar seguro en tu computadora y no compartirla o exponerla en ningún lugar público.	



|| Workflow
	
	Conjunto de procesos y prácticas que un equipo de desarrollo sigue al trabajar con un repositorio Git. 

	Estos procesos definen cómo se gestionan los cambios, cómo se colabora en el código y cómo se integran las nuevas funcionalidades en el proyecto. 
	

	1. Git Flow:

		Es un modelo de flujo de trabajo popular para proyectos de desarrollo de software. 

		Está diseñado para manejar proyectos grandes y complejos con múltiples versiones y ramas de desarrollo. 


	    Ramas Principales: 

	    	Utiliza dos ramas principales: 

	    		'master' para versiones estables y 'develop' para integrar nuevas funcionalidades.
	    

	    Ramas de Características:

	    	Cada nueva funcionalidad se desarrolla en su propia rama de características, que se fusiona con 'develop' una vez completada.


	    Ramas de Publicación: 

	    	Se utilizan ramas de publicación o 'release' para preparar versiones estables para su lanzamiento. 

	    	Estas ramas se derivan de 'develop' y se fusionan tanto en 'master' como en develop después de la publicación.


	    Ramas de Mantenimiento: 

	    	Las correcciones de errores se realizan en ramas de 'mantenimiento' derivadas de master, y luego se fusionan tanto en master como en develop.


	2. GitHub Flow:

		Es un flujo de trabajo simplificado que se utiliza comúnmente en proyectos más pequeños o ágiles. 

		Se centra en la entrega continua y en la iteración rápida. 


	    Branch por Funcionalidad:

	    	Cada nueva funcionalidad se desarrolla en su propia rama. 

	    	Se crea una nueva rama desde 'master' y se fusiona nuevamente en master una vez completada.


	    Pull Requests: 

	    	Se utilizan los 'Pull Requests para revisar y discutir' los cambios propuestos antes de fusionarlos en master.


	    Integración Continua:

	    	Se fomenta la integración continua, donde los cambios se prueban y se implementan regularmente, idealmente varias veces al día.


	3. GitLab Flow:

		Similar al GitHub Flow, pero se basa más en la automatización y la gestión del ciclo de vida del desarrollo de software. 


	    Branch por Funcionalidad:

	    	Cada nueva funcionalidad se desarrolla en su propia rama y se fusiona nuevamente en 'master' cuando está lista para su lanzamiento.


	    Ambientes y Despliegues Automatizados: 

	    	Se utilizan ambientes y despliegues automáticos para facilitar la revisión y la prueba de los cambios en diferentes etapas del ciclo de vida del desarrollo.


	    Ciclo de Vida del Issue: 

	    	Se vinculan los cambios con los 'issues' y se automatiza el proceso de cerrar issues cuando se completan los cambios asociados.


	Consideraciones Adicionales:

	    Personalización: 

	    	Cada equipo puede adaptar y personalizar su flujo de trabajo de Git según sus necesidades específicas y el tamaño y la complejidad del proyecto.


	    Documentación y Comunicación: 

	    	Es importante documentar el flujo de trabajo y comunicar claramente los procesos y prácticas a todo el equipo para garantizar una colaboración efectiva.


|| Fork

	Es una copia exacta de un repositorio existente en tu propia cuenta de usuario. 

	El propósito principal de hacer un fork es permitirte trabajar en una versión del proyecto sin afectar el repositorio original.


    Creación del Fork: 	

    	Se crea una copia exacta del repositorio en tu cuenta de usuario. 

    	Esta copia incluye todo el historial de commits, ramas y archivos del repositorio original.


    Trabajo en el Fork: 

    	Una vez que has creado el fork, puedes trabajar en él de la misma manera que lo harías con cualquier otro repositorio Git. 

    	Puedes clonar el fork en tu computadora, hacer cambios, crear nuevas ramas, realizar commits y cualquier otra operación que necesites.


    Contribuciones al Repositorio Original: 

    	Después de realizar cambios en tu fork y si deseas contribuir al repositorio original, puedes enviar una solicitud de pull request al propietario del repositorio original. 

    	Esto le permite al propietario revisar tus cambios y, si los considera apropiados, fusionarlos en el repositorio original.


    Contribuciones a Proyectos de Código Abierto: 

    	Si deseas contribuir a un proyecto de código abierto alojado en una plataforma como GitHub, generalmente comenzarás haciendo un fork del repositorio del proyecto. 

    	Luego, puedes hacer cambios en tu fork y enviar pull requests al proyecto original para que tus contribuciones sean consideradas.


    Experimentación y Desarrollo Independiente: 

    	También puedes hacer un fork de un repositorio para experimentar con el código, probar nuevas ideas o desarrollar nuevas funcionalidades de forma independiente sin afectar el repositorio original.


    Desarrollo Paralelo: 

    	En algunos casos, puedes hacer un fork de un repositorio para desarrollar una versión personalizada o una bifurcación del proyecto original que se adapte a tus propias necesidades o requerimientos específicos.


    Colaboración: 

    	Los forks facilitan la colaboración en proyectos de código abierto al permitir que cualquiera haga contribuciones al proyecto sin necesidad de permisos especiales.


    Control y Flexibilidad: 

    	Al tener tu propio fork del repositorio, tienes control total sobre el código y puedes trabajar en él de la manera que consideres más apropiada.



|| Snapshots
	
	Las instantáneas se refieren al modo en que Git gestiona y almacena el estado del proyecto en cada commit. 

	A diferencia de algunos sistemas de control de versiones que almacenan cambios incrementales en archivos individuales, Git almacena snapshots del estado completo del proyecto en cada commit. 

	Esto significa que cada commit en Git representa una instantánea del estado completo del proyecto en ese momento específico.


	Instantáneas Complejas: 

		Cuando realizas un commit en Git, Git toma una instantánea completa del estado del proyecto en ese momento. 

		Esto incluye todos los archivos y directorios en el proyecto, así como su contenido y metadatos.


	Almacenamiento Eficiente: 

		Aunque Git almacena cada instantánea completa, utiliza técnicas de compresión y almacenamiento eficientes para minimizar el tamaño del repositorio. 

		Git utiliza algoritmos de compresión y diferenciación para almacenar solo las diferencias entre instantáneas consecutivas cuando sea posible.


	Historial de Instantáneas: 

		El historial de commits en Git representa una secuencia ordenada de instantáneas del proyecto en el tiempo. 

		Cada commit tiene un identificador único (SHA-1 hash) que identifica de manera única esa instantánea en el historial del proyecto.




|| Sincronización Git - GitHub
	
	Establecer una conexión entre un repo local a un repo remoto para enviar y recibir cambios entre elloss. 


	1. Crear un repo en GitHub: 	

		Se pueden establecer multiples configuraciones como descripción del repo,  licencia de software, privacidad, administración, etc. 


	2. Clonar repo remoto en máquina local: 

		```
		git clone <URL_del_repositorio_GitHub>

		```

	3. Realizar cambios locales: 

		Una vez clonado, el repositorio local estará configurado para sincronizar con el repo remoto para realizar cambios, agregar archivos usando 'git add', 'git commit', etc. 


	4. Sincronizar Cambios con GitHub:

		Usar 'git push' para enviar esos cambios al repositorio remoto de GitHub.

		```
		git push origin main

		```

		Enviará los cambios en la rama local "main" al repositorio remoto llamado "origin" en GitHub. 

		Reemplazar "main" con el nombre de la rama en la que estás trabajando si es diferente.


	5. Obtener Cambios desde GitHub:

		Si el proyecto es colaborativo y otros desarrolladores participan en el repositorio remoto de GitHub, obtener esos cambios en tu repositorio local utilizando 'git pull'.

		```
		git pull origin main

		```

		Obtendrá los cambios más recientes de la rama "main" del repositorio remoto "origin" en GitHub y los fusionará automáticamente en tu rama local.


	6. Colaboración y Seguimiento:

		Ahora estás sincronizado con GitHub. 

		Puedes continuar trabajando en tu repositorio local, enviando cambios a GitHub con 'git push' y obteniendo cambios de GitHub con 'git pull' según sea necesario. 

		Colaborar con otros desarrolladores a través de 'Pull Requests', revisiones de código y seguimiento de problemas en GitHub.



|| Origin

	Es una convención comúnmente utilizada para referirse al repositorio remoto predeterminado asociado con tu repositorio local. 

	En la mayoría de los casos, el repositorio remoto predeterminado se llama "origin".

	Cuando clonas un repositorio desde un servidor remoto utilizando el comando git clone, Git automáticamente configura el nombre del servidor remoto como "origin" por defecto. 

	Este nombre "origin" se utiliza para referirse al repositorio remoto cuando realizas operaciones 'git push', 'git pull', o 'git fetch' cambios con el repositorio remoto.



|| Git Clone
	
	Clonar un repositorio Git existente desde un servidor remoto a tu máquina local. 

	Permite obtener una copia completa del proyecto, incluyendo todo el historial de commits, ramas y archivos, lo que te permite trabajar en el proyecto de forma local.

	```
	git clone https://github.com/usuario/nombre-repositorio.git

	```

	Git crea un nuevo directorio en tu máquina local con el nombre del repositorio y coloca todos los archivos y directorios del repositorio dentro de él.

	Git establece la rama predeterminada (generalmente master o main) como la rama actual en tu repositorio local.

	Configura automáticamente el 'origen remoto' del repositorio local para apuntar al repositorio remoto desde el cual fue clonado.



|| Git Pull
	
	Recuperar los cambios desde un repositorio remoto y fusionarlos automáticamente en la rama local actual. 

	'git pull' realiza dos acciones en una sola operación: primero, descarga los cambios desde el repositorio remoto utilizando 'git fetch', y luego fusiona esos cambios en la rama local utilizando 'git merge'.

	Si hay cambios en la rama local que entran en conflicto con los cambios remotos, se pueden producir conflictos de fusión y Git los señalará para que los resuelvas manualmente.

	```
	git pull <remoto> <rama>

	```

	<remoto>: 

		El nombre del repositorio remoto del que deseas obtener los cambios. 

		Por lo general, es "origin" si no se especifica de otro modo.

    <rama>: 

    	La rama del repositorio remoto desde la que deseas obtener los cambios. 

    	Por lo general, es la rama actualmente rastreada.


    Ejemplo: 

    	Si estamos en la rama "main" de tu repositorio local y deseas obtener los cambios más recientes desde el repositorio remoto "origin" y fusionarlos en tu rama local "main".

    	```
		git pull origin main

    	```


    Consideraciones: 

    	Es importante tener en cuenta que 'git pull' fusionará automáticamente los cambios remotos en tu rama local, lo que puede provocar conflictos si hay cambios locales no guardados.
    	
    	Siempre es una buena práctica revisar los cambios descargados antes de fusionarlos para asegurarse de que no haya conflictos o problemas de compatibilidad.
    	
    	En entornos de trabajo colaborativo, es común realizar 'git pull' regularmente para mantenerse actualizado con los cambios realizados por otros miembros del equipo.



|| Git Fetch
	
	Descarga los cambios del repositorio remoto a tu repositorio local sin fusionarlos automáticamente con tu trabajo actual. 

	Es útil cuando no necesariamente deseas fusionarlos de inmediato.


	1. Funcionamiento: 

		Descargar Cambios del Repositorio Remoto: 

			Cuando ejecutas git fetch, Git se comunica con el repositorio remoto y descarga cualquier cambio nuevo que haya ocurrido desde la última vez que obtuviste actualizaciones del repositorio remoto.


	    Actualización de Referencias Locales: 

	    	Git actualiza las referencias locales de las ramas remotas (como origin/master) para que reflejen las últimas actualizaciones del repositorio remoto. 

	    	Sin embargo, no fusiona automáticamente estos cambios en tu rama local actual.


	    Visualización de Cambios:

	    	Después de ejecutar git fetch, puedes ver los cambios descargados utilizando comandos como 'git log', 'git diff' u otros comandos de visualización de historial y diferencias.


	2. Uso de 'git fetch':

		Antes de git pull o git merge: 

			Es común ejecutar 'git fetch' antes de 'git pull' o 'git merge' para obtener los últimos cambios del repositorio remoto y asegurarse de que estás trabajando con la versión más actualizada del código.


		Para Revisar Cambios Remotos: 

			git fetch te permite revisar los cambios del repositorio remoto antes de fusionarlos con tu trabajo local. 

			Esto te da la oportunidad de revisar los cambios y resolver cualquier posible conflicto antes de fusionarlos.


		Para Mantener Referencias Locales Actualizadas: 

			git fetch también es útil para mantener actualizadas las referencias locales de las ramas remotas, lo que facilita el seguimiento de las actualizaciones del repositorio remoto.


	3. Ejemplo: 	

		```
		git fetch

		```

		Descargará los cambios del repositorio remoto a tu repositorio local, pero no los fusionará automáticamente con tu trabajo actual. 

		Puedes revisar los cambios descargados y decidir cómo deseas integrarlos en tu trabajo local.


	4. Consideraciones: 	

		No Fusiona Cambios Automáticamente: 

			A diferencia de git pull, que descarga y fusiona automáticamente los cambios del repositorio remoto, git fetch solo descarga los cambios y actualiza las referencias locales, pero no los fusiona automáticamente.


    	Fusión Manual Requerida:

    		Después de ejecutar git fetch, es posible que necesites fusionar los cambios descargados manualmente utilizando 'git merge' o 'git rebase', según tus necesidades y el flujo de trabajo del proyecto.


   	Esto te da control sobre cómo deseas integrar los cambios en tu trabajo local y te permite revisar los cambios antes de fusionarlos.



|| Git Status
	
	Utilizado para obtener información sobre el estado actual del repositorio de Git. 

	Proporciona una vista general de los cambios realizados en el directorio de trabajo y en el área de preparación (staging area), así como también información sobre la rama actual y el seguimiento de los archivos.


	Funcionamiento: 

		Proporciona información sobre varios aspectos del estado actual del repo.

		Cambios en el Directorio de Trabajo: 

			'git status' muestra los archivos modificados en el directorio de trabajo desde el último commit, así como los archivos que aún no han sido añadidos al área de preparación. 

			Estos archivos aparecen en la sección "Cambios no preparados para el commit".


	    Cambios en el Área de Preparación: 

	    	También muestra los archivos que han sido añadidos al área de preparación (staging area) y que están listos para ser confirmados en el próximo commit. 

	    	Estos archivos aparecen en la sección "Cambios a ser confirmados".


	    Información de la Rama Actual: 

	    	git status muestra la rama actual y su estado en relación con el repositorio remoto. Puede indicar si la rama está actualizada con el repositorio remoto o si hay cambios que deben ser enviados o recibidos.


	Uso: 

		Revisar Cambios Realizados:

			git status se utiliza comúnmente para revisar los cambios realizados en el directorio de trabajo y en el área de preparación antes de realizar un commit. 

			Esto te permite verificar qué archivos han sido modificados y qué archivos están listos para ser confirmados.


    	Verificar el Estado de la Rama: 

    		También se utiliza para verificar el estado de la rama actual en relación con el repositorio remoto. 

    		Esto te permite saber si tu rama está actualizada con el repositorio remoto o si hay cambios que necesitan ser enviados o recibidos.


    Ejemplo: 

		```
		git status

		```

		```
		En la rama main
		Tu rama está actualizada con 'origin/main'.

		Cambios no preparados para el commit:
		  (usa "git add <archivo>..." para actualizar lo que será confirmado)
		  (usa "git restore <archivo>..." para descartar cambios en el directorio de trabajo)
		        modificado:     archivo_modificado.txt

		Cambios a ser confirmados:
		  (usa "git restore --staged <archivo>..." para sacar del área de preparación)
		        modificado:     archivo_modificado.txt

		```


	Consideraciones: 	

		Revisión Antes de Hacer Commit: 

			Es una buena práctica ejecutar 'git status' antes de realizar un commit para asegurarte de que estás incluyendo los cambios deseados y no te olvidas de nada importante.

    	
    	Interpretación de los Resultados: 

    		Es importante entender la información proporcionada por git status para tomar decisiones informadas sobre qué acciones realizar a continuación en tu repositorio Git.



|| Git Diff
	
	Muestra las diferencias entre los cambios en el directorio de trabajo y el área de preparación (staging area), o entre dos commits, o entre dos ramas, o entre cualquier combinación de estos elementos. 

	Es una herramienta esencial para entender los cambios realizados en el código y para revisar el estado del repositorio.


	1. Cambios entre el Directorio de Trabajo y el Área de Preparación:

		```
		git diff

		```
	
		Muestra las diferencias entre los archivos en el directorio de trabajo y los archivos en el área de preparación. 

		Muestra las líneas que se han añadido, eliminado o modificadas desde el último commit.


	2. Cambios entre el Área de Preparación y el Último Commit:

		```
		git diff --staged

		```

		Muestra las diferencias entre los archivos en el área de preparación y los archivos en el último commit. 

		Es útil para revisar los cambios que están listos para ser confirmados en el próximo commit.


	3. Cambios entre Dos Commits:

		```
		git diff commit1 commit2

		```

		Muestra las diferencias entre dos commits específicos. 

		Puedes especificar los commits por su identificador SHA-1, por su nombre de rama, por su nombre de etiqueta o por referencias relativas como HEAD~2 (dos commits antes del commit actual).


	4. Cambios entre dos ramas:

		```
		git diff rama1 rama2

		```

		Muestra las diferencias entre dos ramas específicas.

		Puedes usar nombres de ramas, identificadores SHA-1 o referencias relativas para especificar las ramas.


	Opciones: 	

		-w o --ignore-all-space:

			Ignora los cambios de espacio en blanco.

	    --color-words: 

	    	Muestra las diferencias de palabras resaltadas.

	    --name-only: 

	    	Muestra solo los nombres de los archivos que han cambiado, sin las diferencias reales.

	    --stat: 

	    	Muestra un resumen estadístico de las diferencias.			


	    Ejemplos: 

	    	git diff HEAD~1 HEAD:

	    		Muestra los cambios entre el penúltimo y el último commit.

    		git diff feature-branch master: 

    			Muestra los cambios entre la rama feature-branch y la rama master.

   			git diff --staged:

   				Muestra los cambios que se han añadido al área de preparación pero aún no se han confirmado.	


|| Git Checkout
	
	Se utiliza para cambiar entre ramas, navegar entre commits y deshacer cambios en el directorio de trabajo. 

	Tiene varias funciones dependiendo de cómo se utiliza.


	1. Cambiar de Rama:

		Cuando estás trabajando en un proyecto con múltiples ramas, puedes utilizar 'git checkout' para cambiar de una rama a otra. 

		Permite trabajar en una rama específica y fusionar los cambios cuando estén listos.

		```	
		git checkout nombre_de_rama

		```


	2. Crear una Nueva Rama y Cambiar a Ella:

		Si deseas crear una nueva rama y cambiar a ella inmediatamente, puedes utilizar 'git checkout -b'.
 		
 		Se ahorra el paso de crear una rama por separado y luego cambiar a ella.

		```
		git checkout -b nueva_rama

		```


	3. Navegar Entre Commits:

		Puedes utilizar git checkout para moverte entre commits y explorar el historial del proyecto. 

		Puedes proporcionar el identificador SHA-1 de un commit específico para navegar a ese commit.

		```
		git checkout <commit-SHA-1>

		```	


	4. Deshacer Cambios en el Directorio de Trabajo:

		Si has realizado cambios en el directorio de trabajo pero aún no los has confirmado, puedes utilizar git checkout para deshacer los cambios y restaurar los archivos a su estado en el último commit.

		```
		git checkout -- nombre_de_archivo

		```


	5. Consideraciones:

	    Al cambiar de rama con git checkout, asegúrate de haber confirmado o guardado tus cambios en el directorio de trabajo para evitar perder trabajo no confirmado.

	    Al navegar entre commits con git checkout, ten en cuenta que estarás en un estado "desconectado" conocido como estado "detached HEAD".

	    Asegúrate de comprender los efectos de trabajar en este estado antes de realizar cambios.

	    Si utilizas git checkout para deshacer cambios en el directorio de trabajo, ten cuidado, ya que los cambios no confirmados se perderán permanentemente.



|| Git Switch
	
	Introducido en Git versión 2.23 que se utiliza para cambiar entre ramas o crear y cambiar a una nueva rama en una sola operación. 

	Proporciona una forma más intuitiva y segura de cambiar entre ramas en comparación con el comando 'git checkout'.


	Cambiar de Rama:

		A una rama existente.

		```
		git switch nombre_rama

		```
	

	Crear y Cambiar a una Nueva Rama:

		Crear una nueva rama y cambiar a ella en una sola operación

		```
		git switch -c nombre_nueva_rama

		```


	Consideraciones: 

		'git switch' se considera más intuitivo y seguro que 'git checkout' para cambiar entre ramas porque está diseñado específicamente para ese propósito.
    	
    	A partir de Git 2.23, git switch y 'git restore' se introdujeron como comandos alternativos a git checkout para operaciones relacionadas con el cambio de estado (ramas, confirmaciones, etc.) y restauración de archivos respectivamente.
    	
    	git switch está destinado principalmente para cambiar entre ramas, mientras que git restore se utiliza para restaurar archivos a un estado anterior.



|| Git Reset 

	Se utiliza para deshacer cambios en el repositorio. 

	Puede utilizarse para mover el 'HEAD' y la rama actual a otro commit, deshacer cambios en el área de preparación (staging area), y deshacer cambios en el directorio de trabajo.


	1. git reset --soft <commit>:

		Este comando mueve el 'HEAD' y la rama actual al commit especificado, pero no modifica el área de preparación ni el directorio de trabajo. 

		Los cambios que estaban en el commit seleccionado ahora aparecerán como cambios sin confirmar en el directorio de trabajo.

		```
		git reset --soft HEAD~1

		```


	2. git reset --mixed <commit>:

		Este comando mueve el HEAD y la rama actual al commit especificado y deshace los cambios en el área de preparación. 

		Los cambios que estaban en el commit seleccionado ahora aparecerán como cambios sin confirmar en el directorio de trabajo

		```
		git reset --mixed HEAD~1

		```


	3. git reset --hard <commit>:

		Este comando mueve el HEAD y la rama actual al commit especificado, deshace los cambios en el área de preparación y en el directorio de trabajo. 

		Los cambios realizados después del commit seleccionado se perderán permanentemente.

		```
		git reset --hard HEAD~1

		```


	Usos: 


	    Corregir el Último Commit:

	    	'git reset --soft HEAD~1' te permite corregir el último commit y añadir cambios adicionales a él antes de volver a confirmarlo.
	   

	    Desvincular Cambios del Último Commit: 

	    	'git reset --mixed HEAD~1' te permite desvincular los cambios del último commit y volver a ponerlos en el área de trabajo para ser modificados o confirmados por separado.


	    Eliminar Cambios Locales por Completo: 

	    	'git reset --hard HEAD~1' te permite eliminar por completo los cambios realizados después del último commit.


	Consideraciones:

	    Cuidado con --hard: 

	    	'git reset --hard' puede eliminar permanentemente cambios no confirmados en el directorio de trabajo. 


	    No Desechar Commits Compartidos: 

	    	No uses git reset en commits que ya has compartido con otros desarrolladores a través de un repositorio compartido. 

	    	En su lugar, considera utilizar 'git revert' o 'git rebase'.		



|| Git Amend
	
	Se utiliza para hacer cambios adicionales a un commit existente o para modificar el mensaje del commit más reciente.

	Básicamente, te permite editar el commit más reciente sin necesidad de crear un nuevo commit.

	```
	git commit --amend

	```
	

	1. Modificar los Cambios del Commit Más Reciente:

		Si has realizado cambios adicionales después de hacer un commit pero aún no has confirmado esos cambios, puedes utilizar 'git commit --amend' para incluir esos cambios en el commit más reciente.	

		```
		git add archivo_modificado.txt
		
		git commit --amend

		```

		Abrirá tu editor de texto predeterminado para que puedas editar el mensaje del commit, si lo deseas. 

		Luego, se creará un nuevo commit que incluye los cambios adicionales junto con el mensaje actualizado


	2. Modificar el Mensaje del Commit Más Reciente:

		Si deseas simplemente modificar el mensaje del commit más reciente sin realizar cambios adicionales en los archivos, puedes usar 'git commit --amend' sin realizar ningún cambio en los archivos.

		```
		git commit --amend

		```


	Consideraciones: 

		Ten Cuidado con el Uso de git commit --amend: 

			Dado que git commit --amend reescribe la historia del repositorio, debes tener cuidado al usarlo, especialmente si has compartido tu trabajo con otros desarrolladores. 

			Evita usarlo en commits que ya han sido compartidos y que otros desarrolladores podrían haber basado su trabajo en ellos.


	    No Modifica Commits Anteriores: 

	    	git commit --amend solo modifica el commit más reciente. 

	    	Si deseas realizar cambios en commits anteriores, deberás utilizar herramientas más avanzadas como 'git rebase'.


	    Útil para Corregir Errores Menores: 

	    	git commit --amend es útil para corregir errores menores o para ajustar mensajes de commit sin necesidad de crear commits adicionales.



|| Git Stash
	
	Guardar temporalmente cambios en el directorio de trabajo y el área de preparación (staging area) para que puedas cambiar de rama o trabajar en otra tarea sin necesidad de confirmar los cambios. 

	Básicamente, te permite "guardar" tus cambios en una pila de almacenamiento temporal y luego "sacarlos" más tarde cuando los necesites nuevamente.


	1. Guardar Cambios:

		Cuando tienes cambios en tu directorio de trabajo que no estás listo para confirmar, puedes guardarlos utilizando 'git stash'. 

		Esto moverá los cambios al área de preparación y al directorio de trabajo, dejando tu directorio de trabajo limpio para que puedas cambiar de rama o trabajar en otra tarea.

		```
		git stash

		```


	2. Listar los Stashes:

		Puedes ver una lista de todos los stashes guardados utilizando 'git stash list'.

		Esto te mostrará una lista de los stashes guardados, junto con un identificador único para cada uno.

		```
		git stash list

		```


	3. Aplicar un Stash:

		Para aplicar los cambios guardados en un stash al directorio de trabajo, puedes utilizar 'git stash apply' seguido del identificador del stash. 

		Por defecto, se aplicará el stash más reciente.

		```
		git stash apply

		```


	4. Eliminar un Stash:

		Para eliminar un stash después de aplicarlo, puedes utilizar 'git stash drop' seguido del identificador del stash. 

		Por defecto, se eliminará el stash más reciente.

		```
		git stash drop

		```


		Para eliminar un stash específico, puedes proporcionar su identificador:

		```
		git stash drop stash@{2}

		```


	Aplicar y Eliminar un Stash en una Sola Operación:

		Aplicar los cambios guardados en un stash y eliminarlo al mismo tiempo, puedes utilizar git stash pop seguido del identificador del stash. 

		Por defecto, se aplicará y eliminará el stash más reciente.

		```
		git stash pop

		```


	Consideraciones:

	    git stash es útil cuando tienes cambios no finalizados en tu directorio de trabajo y necesitas cambiar rápidamente de rama o trabajar en otra tarea.

	    Puedes guardar múltiples stashes en la pila de stash y aplicarlos o eliminarlos según sea necesario.

	    Siempre asegúrate de aplicar o eliminar los stashes correctamente para evitar perder cambios importantes o generar conflictos innecesarios.




|| Git Revert

	Deshacer cambios en commits anteriores creando un nuevo commit que revierte los cambios introducidos por un commit específico. 

	A diferencia de 'git reset', que reescribe el historial del repositorio, 'git revert' crea un nuevo commit que deshace los cambios introducidos por un commit anterior, lo que lo hace más seguro para deshacer cambios en commits que ya han sido compartidos con otros desarrolladores a través de un repositorio compartido. 


	1. Deshacer Cambios en un Commit Específico:

		Para deshacer los cambios introducidos por un commit específico y crear un nuevo commit que revierta esos cambios, puedes utilizar git revert seguido del identificador SHA-1 del commit que deseas deshacer.

		```
		git revert <commit-SHA-1>

		```


	2. Resolver Conflictos de Fusión:

		Si el commit que estás intentando revertir ha introducido cambios que entran en conflicto con los cambios actuales en tu rama, es posible que necesites resolver conflictos de fusión manualmente antes de que 'git revert' pueda completar la acción. 

		Una vez resueltos los conflictos, puedes completar el proceso de revertir el commit utilizando 'git revert --continue'.

		```
		git revert --continue

		```


	3. Abortar el Proceso de Revertir:

		Si necesitas abortar el proceso de revertir un commit después de haber comenzado, puedes utilizar 'git revert --abort'. 

		Esto revertirá cualquier cambio realizado por el proceso de revertir y restaurará tu rama al estado en el que estaba antes de comenzar el proceso de revertir.



|| Git Aliases

	Atajos o abreviaciones que puedes crear para tus comandos Git más utilizados.

	Esto te permite simplificar tu flujo de trabajo y hacer que tus comandos sean más fáciles de recordar y escribir. 

	Puedes configurar alias globales, que están disponibles en todos tus repositorios, o alias locales específicos para un repositorio en particular.	


	Alias Globales:

		Puedes configurar alias globales utilizando el comando 'git config --global alias.<alias> "<comando>"'.

		Por ejemplo, si deseas crear un alias llamado "co" para el comando git checkout:

		```
		git config --global alias.co "checkout"

		```

		Puedes escribir git co en lugar de git checkout para cambiar de rama.


	Alias Locales:

		Configurar alias específicos para un repositorio en particular sin afectar otros repositorios. 

		Esto se hace editando directamente el archivo '.git/config' en el repositorio.

		Por ejemplo, puedes agregar el siguiente fragmento al archivo .git/config:	

		```
		[alias]
    		ci = commit

		```

		Creará un alias local llamado "ci" para el comando git commit.


	Listar Alias: 	

		Ver lista de tus alias configurados utilizando el comando 'git config --global --get-regexp alias'.

		```
		git config --global --get-regexp alias

		```


	Eliminar Alias:	

		elimina la línea correspondiente del archivo '.git/config' o utiliza el comando 'git config --global --unset alias.<alias>'.



|| Conflictos
	
	Ocurren cuando dos o más ramas tienen cambios en la misma parte de un archivo o cuando Git no puede determinar automáticamente cómo fusionar los cambios durante una operación como 'git merge' o 'git pull'. 

	Estos conflictos requieren intervención manual por parte del usuario para resolverlos antes de que se pueda completar la fusión.


	1. Causas de Conflictos:

	    Cambios Concurrentes: 

	    	Cuando dos o más personas realizan cambios en la misma parte de un archivo en ramas separadas y luego intentan fusionar esas ramas, Git no puede decidir automáticamente qué cambios deben prevalecer.


	    Historia Divergente: 

	    	Si dos ramas han divergido significativamente en la historia del proyecto y luego intentas fusionarlas, es posible que Git no pueda reconciliar automáticamente los cambios.


	2. Identificar Conflictos:

		Cuando Git encuentra un conflicto durante una operación de fusión, marca los archivos con conflictos y los pone en un estado de "conflicto". 

		Puedes identificar estos archivos por el contenido especial que Git agrega entre '<<<<<<<', '=======', y ''>>>>>>>'.


	3. Resolver Conflictos:
 		
 		Se editan manualmente los archivos conflictivos para elegir qué cambios quieres mantener. 

		Luego, se eliminan las marcas de conflicto agregadas por Git y se agregan los archivos modificados de nuevo al área de preparación utilizando 'git add'.

		Finalmente, puedes completar la fusión con 'git commit'.


	4. Comandos Útiles:

	    git status: 

	    	Verifica qué archivos tienen conflictos y cuáles han sido modificados.

	    git diff: 

	    	Muestra los cambios entre las versiones en conflicto.

	    git mergetool: 

	    	Abre una herramienta de fusión para ayudarte a resolver conflictos de manera más visual.


	5. Consideraciones:

	    Es importante resolver los conflictos de manera cuidadosa y asegurarte de mantener la funcionalidad y la integridad del código.

	    La comunicación y la colaboración con otros miembros del equipo pueden ayudar a prevenir conflictos y resolverlos de manera más efectiva.

	    Resolver conflictos puede ser una parte natural del desarrollo colaborativo, así que no te preocupes si encuentras conflictos en tus proyectos.



|| Permisos 
	
	Son Niveles de acceso y las capacidades que tienen los usuarios sobre un repositorio de Git específico. 

	Estos permisos controlan quién puede leer, escribir o ejecutar acciones específicas en un repositorio, como clonar, enviar cambios, fusionar ramas, crear etiquetas y más. 

	Los permisos se gestionan típicamente a nivel de servidor o plataforma de alojamiento de código, como GitHub, GitLab o Bitbucket.

	
	1. Lectura (Read):

		Los usuarios con permisos de lectura pueden ver el contenido de un repositorio, incluyendo archivos, ramas, confirmaciones y etiquetas.

		Sin embargo, no pueden realizar cambios ni ejecutar acciones que modifiquen el estado del repositorio.


	2. Escritura (Write):

		Los usuarios con permisos de escritura tienen la capacidad de realizar cambios en el repositorio, como crear ramas, enviar cambios y crear etiquetas. Sin embargo, pueden estar restringidos en algunas acciones más sensibles, como fusionar ramas o eliminar etiquetas.


	3. Administración (Admin):

		Los usuarios con permisos de administración tienen control total sobre el repositorio. 

		Pueden realizar todas las acciones disponibles, incluyendo la configuración del repositorio, la gestión de permisos de usuarios y la eliminación del repositorio.
	

	Gestión de Permisos:

		La gestión de permisos generalmente se realiza a nivel de equipo o proyecto en la plataforma de alojamiento de código correspondiente. 

		Los propietarios del repositorio o los administradores del proyecto pueden asignar diferentes niveles de permisos a los miembros del equipo según sea necesario.


	Uso de Grupos:

		En muchas plataformas de alojamiento de Git, los permisos se pueden gestionar a través de grupos, lo que facilita la asignación de permisos a múltiples usuarios de manera coherente. 

		Los usuarios se pueden agregar a grupos específicos y luego se pueden asignar permisos a esos grupos en lugar de a usuarios individuales.


	Consideraciones:

	    Es importante asignar los permisos de manera cuidadosa y otorgar acceso solo a las personas que necesitan realizar ciertas acciones en el repositorio.

    	Algunas plataformas de alojamiento de Git permiten la personalización de permisos más avanzada, como la capacidad de crear roles personalizados con conjuntos específicos de permisos.

    	La comprensión de los niveles de permisos y la gestión efectiva de los mismos son partes importantes de la administración de proyectos de software colaborativos.


    GitHub:

    	Establecer quién tiene acceso y qué acciones pueden realizar los usuarios en un repositorio específico o en toda una organización. 

    	Esto es fundamental para gestionar la colaboración y la seguridad en proyectos de software alojados en GitHub. 


		Accede al Repositorio: 

			Ve al repositorio en GitHub que deseas configurar.

		    Haz clic en "Settings":

		   		En la parte superior derecha del repositorio, haz clic en "Settings" para acceder a la configuración del repositorio.


		    Selecciona "Manage access": 

		    	En el menú de la izquierda, selecciona "Manage access" para acceder a la configuración de permisos.


		    Invitar Colaboradores:

		    	Puedes invitar colaboradores al repositorio agregando sus nombres de usuario de GitHub o direcciones de correo electrónico.

		    	Puedes asignarles uno de los siguientes roles:

		        Admin: 

		        	Tiene acceso de lectura/escritura total al repositorio y puede administrar la configuración del repositorio.


		        Write: 

		        	Tiene acceso de lectura/escritura al repositorio, pero no puede administrar la configuración del repositorio.


		        Read: 

		        	Tiene acceso de solo lectura al repositorio.


		    Añadir Colaboradores:

		    	Después de seleccionar el rol apropiado, haz clic en "Add [nombre de usuario/email]" para agregar a los colaboradores al repositorio.


		Configuración de Permiso en una Organización:

		    Accede a la Configuración de la Organización: 

		    	Ve al perfil de la organización en GitHub y haz clic en "Settings".


		    Selecciona "Member privileges": 

		    	En el menú de la izquierda, selecciona "Member privileges" para acceder a la configuración de permisos de los miembros de la organización.


		    Configura los Roles de los Miembros: 

		    	Puedes configurar los roles de los miembros de la organización según tus necesidades. 

		    	Los roles disponibles son similares a los de los repositorios individuales (Admin, Write, Read).


		    Administra los Roles de los Equipos: 	

		    	Además de los roles individuales, puedes crear equipos dentro de la organización y asignar roles a esos equipos. 

		    	Esto facilita la gestión de permisos para grupos de miembros.


		Consideraciones:

		    Es importante asignar los permisos adecuados a los colaboradores según sus responsabilidades en el proyecto.

		    GitHub ofrece opciones de configuración flexibles que permiten adaptar los permisos a las necesidades específicas de tu proyecto o organización.

		    La auditoría de actividad y los registros de acceso están disponibles para ayudar a los administradores a rastrear quién ha realizado qué acciones en el repositorio u organización



|| Archivos
	
	Elementos individuales dentro de un repositorio que contienen datos, como código fuente, archivos de configuración, imágenes, documentos, entre otros. 

	Los archivos son la unidad básica de almacenamiento y seguimiento en Git y forman parte del historial de versiones del repositorio.


	Seguimiento de Archivos:

		Git rastrea los cambios en los archivos mediante el sistema de control de versiones. 

		Esto significa que Git registra las modificaciones realizadas en cada archivo a lo largo del tiempo, lo que te permite ver el historial de cambios y revertir a versiones anteriores si es necesario.
	

	Estados de Archivos:

	    No Seguido (Untracked):

	    	Archivos que aún no se han añadido al área de preparación (staging area) para ser incluidos en el próximo commit.


	    Pendiente (Staged): 

	    	Archivos que se han añadido al área de preparación y están listos para ser incluidos en el próximo commit.


	    Modificado (Modified):

	    	Archivos que han sido modificados desde el último commit y aún no se han añadido al área de preparación.


	    Confirmado (Committed):

	    	Archivos que han sido incluidos en un commit y están almacenados en la base de datos de Git.


	Operaciones con Archivos:

	    Añadir (Add): 

	    	Agregar archivos al área de preparación para incluirlos en el próximo commit.


	    Commit: 

	    	Confirmar los cambios realizados en los archivos en el repositorio local.


	    Eliminar (Remove): 

	    	Eliminar archivos del repositorio local y del área de preparación.


	    Mover (Move/Rename): 

	    	Cambiar el nombre o mover archivos dentro del repositorio, manteniendo su historial de versiones.


	Historia de Versiones:

		Cada archivo en un repositorio Git tiene su propio historial de versiones, que registra todos los cambios realizados en ese archivo a lo largo del tiempo. 

		Esto te permite rastrear quién hizo qué cambios, cuándo se realizaron y revertir a versiones anteriores si es necesario.


	Ramificaciones y Fusión:

		Los archivos son compartidos entre diferentes ramas en un repositorio Git. 

		Puedes crear nuevas ramas para trabajar en nuevas características o correcciones de errores sin afectar el código en otras ramas. 

		Luego, puedes fusionar los cambios de una rama a otra, lo que también fusiona los cambios en los archivos.
	
	
	Colaboración:

		Los archivos en un repositorio Git pueden ser compartidos y colaborados por múltiples personas. 

		Los cambios realizados por diferentes colaboradores pueden ser gestionados y fusionados de forma segura utilizando las capacidades de control de versiones de Git.



|| Adm. Ramas

	1. Create Branches:	

		Las ramas permiten trabajar en diferentes líneas de desarrollo de forma paralela sin afectar el código en otras ramas. 


		Crear una Rama Nueva:

			Para crear una nueva rama en Git, puedes utilizar el comando git branch seguido del nombre de la nueva rama que deseas crear. 

			Por ejemplo, si deseas crear una rama llamada "nueva-funcionalidad":

			```
			git branch nueva-funcionalidad

			```
			
			no cambiará tu posición actual en el repositorio.

			Seguirás trabajando en la misma rama en la que estabas antes de ejecutar el comando.


	2. Change Branch:

		Cambiar a una Rama Nueva:

			Después de crear una nueva rama, es común querer cambiar a esa rama para comenzar a trabajar en ella. 

			Puedes hacer esto utilizando el comando 'git checkout'.

			```
			git checkout nueva-funcionalidad

			```	

			Cambiará tu posición actual en el repositorio a la nueva rama "nueva-funcionalidad". 

			A partir de ahora, cualquier cambio que realices y cualquier commit que hagas se aplicará a esta nueva rama.


		Crear y Cambiar a una Rama en un Solo:

			```
			git checkout -b nueva-funcionalidad

				```

				Cambia tu posición actual en el repositorio a esa rama en un solo paso.	
	

	3. Change Branch Name:
		
		Cambiar el Nombre de una Rama Local:

    		Asegúrate de estar en otra rama: 

    			Antes de cambiar el nombre de la rama, asegúrate de no estar actualmente en la rama que deseas renombrar. 

    			Si estás en esa rama, cámbiate a otra rama utilizando git checkout:

    			```
    			git checkout otra-rama
    		
    			```


    		Renombrar la Rama:

    			Utiliza el comando git branch -m seguido del nombre actual de la rama y el nuevo nombre que deseas asignarle.

    			Por ejemplo, si quieres cambiar el nombre de la rama "mi-rama" a "mi-rama-nueva":

    			```
    			git branch -m mi-rama mi-rama-nueva

    			```
			

    	Cambiar el Nombre de una Rama Remota:

		    Cambiar el Nombre de la Rama Localmente: 

		    	Sigue los pasos anteriores para cambiar el nombre de la rama localmente utilizando git branch -m.


		    Eliminar la Rama Remota Antigua: 

		    	Utiliza el comando git push con la opción --delete para eliminar la rama remota con el nombre antiguo. 

		    	Por ejemplo, si la rama remota antigua se llamaba "mi-rama":

		    	```
		    	git push origin --delete mi-rama

		    	```


		    Enviar la Rama Local Renombrada: 	

		    	Utiliza el comando git push para enviar la rama local renombrada con el nuevo nombre al repositorio remoto:

		    	```
		    	git push origin mi-rama-nueva
		    	
		    	```

		Consideraciones: 

			Comunicar Cambios: 

				Es importante comunicar cualquier cambio en el nombre de la rama a otros miembros del equipo que puedan estar trabajando en ella para evitar confusiones.


    		Impacto en la Colaboración: 

    			Cambiar el nombre de una rama puede afectar a otros miembros del equipo que estén trabajando en la misma rama.

    			Asegúrate de coordinar con el equipo y evitar cambios repentinos que puedan causar problemas de integración.			

	4. Delete Branch:
		
		Puede ser necesario una vez que has completado el trabajo en una rama y ya no la necesitas, o si deseas mantener limpio el historial de ramas.


		Eliminar una Rama Localmente:

			Para eliminar una rama localmente en Git, puedes utilizar el comando git branch con la opción -d seguida del nombre de la rama que deseas eliminar. 

			Por ejemplo, si deseas eliminar una rama llamada "mi-rama":

			```
			git branch -d mi-rama

			```

			Si la rama que intentas eliminar contiene commits que no han sido fusionados en otras ramas, Git mostrará un mensaje de advertencia. 


			Para forzar la eliminación de la rama sin verificar si los commits han sido fusionados, puedes utilizar la opción -D en lugar de -d:

			```
			git branch -D mi-rama

			```

		
		Eliminar una Rama Remota:

			Para eliminar una rama en el repositorio remoto desde tu repositorio local, puedes utilizar el comando git push con la opción --delete seguida del nombre de la rama remota que deseas eliminar. 

			Por ejemplo, si deseas eliminar la rama "mi-rama" del repositorio remoto:
			
			```
			git push origin --delete mi-rama

			```


		Consideraciones: 

			Precaución al Eliminar Ramas: 

				Antes de eliminar una rama, asegúrate de que no necesitas los cambios contenidos en esa rama. 

				Una vez eliminada, no podrás recuperarla a menos que tengas una copia de seguridad.


	    	Impacto en la Colaboración: 

	    		Al eliminar una rama remota, asegúrate de comunicar esta acción a los demás miembros del equipo, especialmente si están trabajando en la misma rama. La eliminación de una rama remota puede afectar el flujo de trabajo de otros colaboradores.


	    	Conservar un Historial Limpio: 

	    		Eliminar ramas obsoletas o terminadas ayuda a mantener un historial de ramas limpio y ordenado, lo que facilita la gestión del repositorio y la revisión del historial de cambios.


	5. Merge Branches:
		
		Permite combinar los cambios realizados en una rama con otra. 

		Esto es útil cuando has trabajado en una funcionalidad o una línea de desarrollo en una rama separada y deseas integrar esos cambios en otra rama, como la rama principal del proyecto

		
		Fusionar Cambios de una Rama en Otra:

    		Cambia a la Rama Destino: 

    			Antes de fusionar los cambios de una rama en otra, asegúrate de estar en la rama en la que deseas integrar los cambios. 

    			Puedes cambiar a la rama destino utilizando el comando git checkout:

    			```
    			git checkout rama_destino

    			```


    		Fusionar la Rama Origen:

    			Una vez que estés en la rama destino, utiliza el comando git merge seguido del nombre de la rama que deseas fusionar en la rama destino. 

    			Por ejemplo, para fusionar los cambios de la rama "mi_rama" en la rama actual:

    			```
    			git merge mi_rama

    			```


		Conflictos de Fusión:

			Durante el proceso de fusión, es posible que Git detecte conflictos si los cambios realizados en la rama que estás fusionando entran en conflicto con los cambios existentes en la rama destino.

			En este caso, Git pausará el proceso de fusión y te indicará qué archivos tienen conflictos. 

			Deberás resolver estos conflictos manualmente editando los archivos en conflicto para resolver las diferencias.

			Una vez resueltos los conflictos, añade los archivos modificados al área de preparación con 'git add' y luego completa la fusión con 'git commit'. 

			Después de resolver los conflictos y completar el commit de fusión, los cambios de la rama origen se habrán integrado en la rama destino.



|| Adm. Archivos


	1. Remover Archivos:

		Eliminar un Archivo del Sistema de Archivos y del Control de Versiones:

			Tanto del sistema de archivos local como del control de versiones de Git, puedes utilizar el comando 'git rm' seguido del nombre del archivo.

			```
			git rm archivo_a_eliminar.txt

			```


		Eliminar un Archivo del Control de Versiones, pero Conservarlo en el Sistema de Archivos:

			Si deseas eliminar un archivo del control de versiones de Git pero conservarlo en el sistema de archivos local, puedes utilizar el comando 'git rm --cached' seguido del nombre del archivo.

			```
			git rm --cached archivo_a_eliminar.txt

			```


		Eliminar un Archivo del Sistema de Archivos sin Afectar el Control de Versiones:

			Si solo deseas eliminar un archivo del sistema de archivos local sin afectar el control de versiones de Git, puedes utilizar el comando 'rm' del sistema operativo seguido del nombre del archivo.

			```
			rm archivo_a_eliminar.txt

			```

			para evitar que Git rastree los cambios en este archivo, puedes agregarlo al archivo '.gitignore' para que Git ignore cualquier cambio en él.


		Confirmar los Cambios:

			Después de eliminar el archivo y/o marcar el cambio para ser confirmado, debes realizar un commit para confirmar los cambios en el repositorio. 

			Esto registra la eliminación del archivo en el historial de cambios de Git.

			```
			git commit -m "Eliminar archivo_a_eliminar.txt"

			```


		Antes de eliminar un archivo, asegúrate de que realmente deseas eliminarlo y de que no se necesita en el proyecto.
		
		Recuerda que los archivos eliminados en Git aún pueden ser recuperados del historial de commits si es necesario, por lo que no se eliminan permanentemente a menos que se realice una limpieza adicional


	2. Renombrar Archivos:

		Utilizando el Comando git mv:

			El comando git mv te permite renombrar un archivo y automáticamente registrar el cambio en Git.

			```
			git mv archivo_antiguo archivo_nuevo

			```

			```
			git mv old_file.txt new_file.txt

			```


		Manualmente Renombrando y Añadiendo el Cambio:

			Si prefieres no usar git mv, también puedes renombrar manualmente el archivo en tu sistema de archivos y luego añadir el cambio a Git por separado. 

			a. Renombrar Manualmente el Archivo:

				Renombra el archivo utilizando los comandos de tu sistema operativo, como 'mv'

				```
				mv old_file.txt new_file.txt

				```


			b. Añadir el Cambio a Git:

				Añade el cambio al área de preparación (staging area) utilizando el comando 'git add':

				```
				git add new_file.txt

				```


		Confirmar el Cambio:

			Una vez que hayas renombrado el archivo y añadido el cambio a Git, realiza un commit para registrar el cambio en el historial de versiones:

			```
			git commit -m "Renombrar old_file.txt a new_file.txt"			

			```


		Al renombrar archivos en Git, se mantiene el historial de cambios del archivo. 

		No se crea un nuevo archivo; Git simplemente registra el cambio de nombre en el historial de commits.

	    Es recomendable utilizar 'git mv' en lugar de renombrar manualmente los archivos para asegurarte de que Git rastree correctamente el cambio de nombre.

	    Renombrar archivos en Git no afecta al contenido del archivo ni a su historial de cambios. 

	    Solo cambia el nombre del archivo dentro del repositorio.

	    Si el archivo que estás renombrando está siendo rastreado por Git en ramas o commits anteriores, Git reconocerá automáticamente el cambio de nombre y lo registrará adecuadamente en el historial de versiones.



	3. Mover Archivos:

		Cambiar la ubicación de un archivo dentro del repositorio mientras se mantiene su historial de cambios.


		Utilizando el Comando git mv:

			El comando 'git mv' te permite mover archivos o directorios dentro del repositorio y automáticamente registra el cambio en Git. 

			La sintaxis es similar a mv en el sistema operativo, pero git mv asegura que Git siga el cambio adecuadamente.

			```
			git mv archivo_o_directorio_destino nuevo_directorio

			```

			Mover un archivo llamado 'archivo.txt' al directorio 'nuevo_directorio':

			```
			git mv archivo.txt nuevo_directorio/

			```


		Renombrar y Añadir el Cambio Manualmente:

			Si prefieres no utilizar git mv, puedes mover archivos manualmente y luego añadir el cambio a Git por separado.


			a. Renombrar Manualmente el Archivo:

				Mueve el archivo utilizando los comandos de tu sistema operativo, como 'mv'

				```
				mv archivo.txt nuevo_directorio/

				```


			b. Añadir el Cambio a Git:

				Añade el cambio al área de preparación (staging area) utilizando el comando git add:

				```
				git add nuevo_directorio/archivo.txt

				```


		Confirmar el Cambio:

			Una vez que hayas movido el archivo y añadido el cambio a Git, realiza un commit para registrar el cambio en el historial de versiones:

			```
			git commit -m "Mover archivo.txt a nuevo_directorio/"

			```


		Al mover archivos en Git, se mantiene el historial de cambios del archivo. 

		No se crea un nuevo archivo; Git simplemente registra el cambio de ubicación en el historial de commits.
    	
    	Es recomendable utilizar git mv en lugar de mover manualmente los archivos para asegurarte de que Git rastree correctamente el cambio de ubicación.
    	
    	Al mover un archivo, Git reconoce automáticamente el cambio y actualiza su registro interno. 

    	Esto significa que los cambios en el archivo se seguirán rastreando sin problemas.
    	
    	Si el archivo que estás moviendo está siendo rastreado por Git en ramas o commits anteriores, Git reconocerá automáticamente el cambio de ubicación y lo registrará adecuadamente en el historial de versiones.


    4. Ignoring files: 	

    	Significa decirle a Git que ignore ciertos archivos o patrones de archivos específicos para que no sean rastreados por el control de versiones. 

    	Esto es útil para evitar que archivos generados automáticamente, archivos temporales o archivos sensibles se incluyan accidentalmente en el repositorio.


		Archivo .gitignore:

			El método más común para ignorar archivos en Git es utilizando un archivo llamado '.gitignore'.

			Este archivo contiene una lista de patrones de archivos que Git debe ignorar. 

			Cada línea del archivo .gitignore representa un patrón de archivo o un patrón de directorio (si termina con una barra /).    
			
			```
			# Ignorar archivos de respaldo generados por el editor
			*~

			# Ignorar archivos de compilación y ejecutables
			*.o
			*.out
			*.exe

			# Ignorar directorios específicos
			node_modules/

			```


		Sintaxis de Patrones en .gitignore:

		    *: 

		    	Coincide con cualquier cadena de caracteres.

		    ?: 

		    	Coincide con un solo carácter.

		    []: 

		    	Coincide con un solo carácter dentro de los corchetes.

		    **: 

		    	Coincide con cualquier cadena de caracteres que incluya barras (/), utilizada para hacer coincidencias recursivas en directorios.

		    /: 

		    	Utilizado al final de un patrón para indicar que es un directorio.


		Ubicación del Archivo .gitignore:

			El archivo .gitignore se puede colocar en el directorio raíz del repositorio o en cualquier subdirectorio, y se aplica a ese directorio y a sus subdirectorios recursivamente.


		Ignorar Archivos ya Rastreados:

			Si ya has agregado un archivo al repositorio y luego decides ignorarlo, necesitas eliminarlo del índice de Git antes de que se ignore. 

			Puedes hacerlo utilizando el comando git rm --cached:

			```
			git rm --cached archivo_a_ignorar.txt

			```


		Archivos Globales de Ignorados:

			Además del archivo .gitignore local en cada repositorio, puedes configurar un archivo .gitignore_global a nivel global en tu sistema para ignorar patrones de archivos en todos tus repositorios.

			Esto es útil para patrones de archivos que deseas ignorar en todos tus proyectos.


		Actualizar el archivo .gitignore según sea necesario a medida que el proyecto evoluciona y se agregan nuevos archivos que deben ser ignorados.
		
		Los archivos listados en .gitignore no se rastrean por Git y no se incluyen en los commits. 

		Sin embargo, si ya están rastreados, necesitas eliminarlos del índice de Git para que se ignoren.
		
		Es útil revisar regularmente el estado de tu repositorio para asegurarte de que no estés incluyendo archivos no deseados en tus commits.

		Puedes hacerlo utilizando el comando 'git status'.		


	5. Cat-File:

		Comando avanzado en Git que se utiliza para mostrar información sobre objetos Git en el repositorio.

		Los objetos en Git incluyen commits, árboles, blobs (archivos), etiquetas y objetos de tipo especial como commits firmados y commits con firmas GPG. 

		El comando git cat-file proporciona una forma de inspeccionar estos objetos y mostrar detalles sobre ellos.


		Sintaxis Básica:
 			
 			'git cat-file'

 			```
 			git cat-file [-t | -s | -e] <objeto>

 			```

 			-t: Muestra el tipo del objeto.

			-s: Muestra el tamaño del objeto en bytes.

			-e: Verifica si el objeto existe


		Ejemplos: 	

			1. Mostrar el Tipo de un Objeto:

				```
				git cat-file -t <sha-1>

				```

				Muestra el tipo del objeto especificado por su identificador SHA-1.


			2. Mostrar el Tamaño de un Objeto:

				```
				git cat-file -s <sha-1>

				```

				Muestra el tamaño en bytes del objeto especificado por su identificador SHA-1.


			3. Verificar si un Objeto Existe:

				```	
				git cat-file -e <sha-1>

				```


			4. Mostrar el Contenido de un Blob:

				```
				git cat-file -p <sha-1>

				```


		El comando 'git cat-file' es útil para la inspección y la manipulación de objetos Git a bajo nivel, pero puede ser complicado de utilizar para usuarios sin experiencia en el funcionamiento interno de Git.
    	
    	Es importante tener cuidado al manipular objetos Git directamente, ya que pueden afectar la integridad y la consistencia del repositorio.
    	
    	Para los usuarios habituales de Git, 'git cat-file' puede ser una herramienta valiosa para la depuración, el análisis y la comprensión de los detalles internos del repositorio.



|| Buenas practicas 

	Commits:

		1. Mensajes de Commit Descriptivos:

		    Utiliza mensajes de commit descriptivos y significativos que expliquen claramente los cambios realizados en el commit.

		    Comienza el mensaje de commit con un verbo en tiempo presente, como "Agregar", "Corregir" o "Actualizar", seguido de una breve descripción del cambio.

		    Limita la longitud del mensaje de commit a aproximadamente 50-72 caracteres para mantenerlo conciso y legible en la línea de asunto.


		2. Commits Atómicos y Frecuentes:

		    Realiza commits atómicos, es decir, un commit por cambio lógico o funcional. 

		    Evita realizar commits masivos que incluyan múltiples cambios no relacionados.

		    Realiza commits con frecuencia y de manera regular para capturar y registrar los cambios de forma incremental a medida que trabajas en tu proyecto.


		3. Revisión y Confirmación de Cambios:

		    Antes de realizar un commit, revisa cuidadosamente los cambios realizados para asegurarte de que sean correctos y estén completos.

		    Divide los cambios en etapas lógicas y confirma cada etapa por separado, asegurándote de que cada commit represente un estado coherente y funcional del proyecto.


		4. Evitar Commits de Depuración o Temporales:

		    Evita realizar commits de código de depuración, comentarios de desarrollo o cambios temporales que no sean relevantes para el estado final del proyecto.

		    Utiliza herramientas como 'git stash' para guardar temporalmente cambios no relacionados con el commit actual sin comprometer la integridad del historial de commits.


		5. Utilizar Ramas Feature o Temáticas:

		    Utiliza ramas separadas para desarrollar nuevas características o abordar problemas específicos. 

		    Realiza commits en estas ramas y fusiona los cambios en la rama principal cuando estén completos y probados.

		    Mantén el historial de commits de cada rama temática o de características lo más limpio y coherente posible.


		6. Referenciar Issues o Solicitudes de Extracción:

		    Si estás trabajando en un proyecto de equipo o en un repositorio de código abierto que utiliza sistemas de seguimiento de problemas o solicitudes de extracción, haz referencia a los números de problema o las URL de las solicitudes de extracción en tus mensajes de commit.

		    Esto ayuda a mantener un registro claro de qué cambios están relacionados con qué problemas o solicitudes de extracción y facilita la colaboración y la revisión del código.


	Branch: 

		1. Mantén una Rama Principal Estable:

		    La rama principal, como "main" o "master", debe mantenerse estable y lista para producción en todo momento. 

		    Evita enviar cambios directamente a esta rama y utiliza ramas de características o de desarrollo para trabajar en nuevas funcionalidades.


		2. Crea Ramas para Cada Funcionalidad:

		    Crea una nueva rama para cada nueva funcionalidad, corrección de errores o tarea. 

		    Esto te permite trabajar de forma aislada en cada cambio y facilita la colaboración con otros miembros del equipo.


		3. Usa Nombres Descriptivos para las Ramas:

		    Asigna nombres descriptivos y significativos a tus ramas para que sea fácil entender su propósito.

		    Por ejemplo, utiliza nombres como "feature/nueva-funcionalidad" o "bugfix/correccion-de-error".


		4. Mantén las Ramas Actualizadas con la Rama Principal:

		    Asegúrate de mantener tus ramas de características actualizadas con la rama principal. 

		    Realiza frecuentes "git pull" desde la rama principal para incorporar los últimos cambios antes de fusionar tu rama de características.


		5. Fusiona las Ramas con Frecuencia:

		    Fusiona tus ramas de características con la rama principal tan pronto como sea posible una vez que estés seguro de que el código está listo. 

		    Esto ayuda a evitar conflictos y mantiene un historial de cambios limpio.


		6. Realiza Revisiones de Código:

		    Antes de fusionar una rama de características en la rama principal, realiza revisiones de código para asegurarte de que el código cumpla con los estándares de calidad y funcionalidad esperados.


		7. Borra Ramas Obsoletas:

		    Después de fusionar una rama de características o una corrección de errores, asegúrate de borrar la rama obsoleta para mantener limpio el historial de ramas y evitar confusiones en el futuro.


		8. Utiliza Ramas de Lanzamiento y de Corrección de Errores:

		    Además de las ramas de características, considera utilizar ramas de lanzamiento para preparar versiones estables del software y ramas de corrección de errores para corregir problemas urgentes en versiones publicadas.


		9. Comunica Cambios en las Ramas:

		    Mantén a tu equipo informado sobre las ramas en las que estás trabajando y cualquier cambio importante que realices. 

		    La comunicación clara ayuda a evitar conflictos y a mantener a todos en la misma página.


	Merge: 

		1. Mantén la Rama Principal Estable:

	    	Antes de fusionar una rama de características en la rama principal, asegúrate de que la rama principal esté estable y lista para producción.

	    	Esto minimiza la posibilidad de introducir errores en el código base.


		2. Realiza Frecuentes Fusiones Pequeñas:

		    En lugar de esperar a fusionar grandes cambios al final, realiza fusiones pequeñas y frecuentes. 

		    Esto facilita la resolución de conflictos y ayuda a mantener un historial de cambios limpio y comprensible.


		3. Resuelve Conflictos Rápidamente:

		    Si se producen conflictos durante la fusión, resuélvelos lo antes posible. 

		    Examina los archivos en conflicto, toma decisiones informadas sobre qué cambios mantener y comunica cualquier ajuste necesario al equipo.


		4. Utiliza Herramientas de Resolución de Conflictos:

		    Git ofrece herramientas integradas, como git mergetool, para ayudar a resolver conflictos de manera más eficiente.

		    Explora estas herramientas y elige la que mejor se adapte a tu flujo de trabajo.


		5. Realiza Revisiones de Código Post-Fusión:

		    Después de fusionar una rama de características, realiza revisiones de código en la rama resultante para asegurarte de que cumple con los estándares de calidad y funcionalidad esperados.


		6. Comunica los Cambios:

		    Mantén a tu equipo informado sobre las fusiones que realizas y cualquier cambio importante en el código base. 

		    La comunicación clara ayuda a mantener a todos en la misma página y facilita la colaboración.


		7. Utiliza Ramas de Lanzamiento:

		    Considera utilizar ramas de lanzamiento para preparar versiones estables del software antes de fusionarlas en la rama principal. 

		    Esto permite realizar pruebas adicionales y corregir problemas antes del despliegue.


		8. Realiza Pruebas Rigurosas:

		    Después de fusionar cambios en la rama principal, realiza pruebas rigurosas para asegurarte de que el código funciona como se esperaba y no ha introducido nuevos errores en el proyecto.


		9. Revierte Cambios si es Necesario:

		    Si una fusión introduce problemas graves en el código, no dudes en revertir los cambios y volver a un estado estable.

		    Esto te permite mantener la integridad del proyecto mientras investigas y solucionas el problema.


		10. Documenta los Cambios Realizados:

		    Después de realizar una fusión, documenta los cambios realizados en el código y cualquier ajuste importante realizado durante el proceso. 

		    Esto facilita el seguimiento de los cambios y la resolución de problemas en el futuro.


	Pull Request:

		1. Abre Pull Requests Pequeños y Frecuentes:

		    Divide tus cambios en unidades lógicas y pequeñas, y abre PRs para cada una. 

		    Esto facilita la revisión y la fusión, además de reducir el riesgo de introducir errores.


		2. Descripción Detallada y Contextual:

		    Proporciona una descripción clara y detallada de los cambios introducidos por el PR.

		    Incluye información sobre qué problema resuelve, por qué se necesitan los cambios y cómo se ha probado.


		3. Asigna Revisores Apropiados:

		    Asigna a revisores que estén familiarizados con el área afectada por los cambios. 

		    Esto garantiza una revisión más efectiva y detallada.


		4. Utiliza Ramas de Funcionalidades:

		    Trabaja en ramas separadas para cada funcionalidad o corrección de errores y abre un PR cuando estés listo para integrar los cambios en la rama principal.


		5. Solicita Retroalimentación Activa:

		    Actívamente solicita retroalimentación a los revisores asignados al PR. 

		    Está abierto a sugerencias y discusiones para mejorar el código.


		6. Mantén un Diálogo Constructivo:

		    Mantén un diálogo constructivo y respetuoso con los revisores durante el proceso de revisión.

		    Aborda sus comentarios y preguntas de manera oportuna y considerada.


		7. Realiza Pruebas de Integridad Continua:

		    Configura pruebas automatizadas, como pruebas unitarias, pruebas de integración y análisis estático de código, y asegúrate de que pasen antes de solicitar la revisión del PR.


		8. Evita la Inclusión de Cambios no Relacionados:

		    Mantén el PR centrado en un único conjunto de cambios relacionados.

		    Evita incluir cambios que no estén directamente relacionados con el propósito del PR.


		9. Monitorea el Estado del PR:

		    Monitorea el estado del PR y responde a cualquier comentario o solicitud de cambios de los revisores de manera oportuna.


		10. Fusiona el PR una Vez Aprobado:

		    Una vez que el PR ha sido revisado y aprobado por los revisores, fusiona los cambios en la rama principal de manera oportuna.


	Colaboración: 

		1. Utiliza Ramas de Funcionalidades:

		    Trabaja en ramas separadas para cada nueva funcionalidad o corrección de errores.

		    Esto permite a los miembros del equipo trabajar de forma aislada sin interferir con el trabajo de los demás.


		2. Mantén Ramas Actualizadas:

		    Actualiza regularmente tus ramas de funcionalidades con los últimos cambios de la rama principal. 

		    Esto minimiza los conflictos y facilita la integración de tus cambios en el proyecto.


		3. Comunica los Cambios:

		    Mantén al equipo informado sobre los cambios que realizas en el código. 

		    Utiliza Pull Requests, comentarios en el código y actualizaciones en herramientas de gestión de proyectos para comunicar los cambios de manera efectiva.


		4. Realiza Revisiones de Código:

		    Solicita revisiones de código a otros miembros del equipo antes de fusionar tus cambios en la rama principal. 

		    Las revisiones de código ayudan a mantener la calidad del código y a detectar posibles problemas antes de que lleguen a la producción.


		5. Utiliza Comentarios y Etiquetas:

		    Utiliza comentarios y etiquetas en los Pull Requests para proporcionar retroalimentación específica sobre los cambios realizados. 

		    Esto ayuda a mantener un registro de los comentarios y facilita la colaboración entre los miembros del equipo.


		6. Establece Normas de Codificación:

		    Establece normas de codificación claras y consistentes en tu equipo. 

		    Esto incluye convenciones de nomenclatura, estilo de código y prácticas de codificación que deben seguir todos los miembros del equipo.


		7. Automatiza Pruebas y Despliegues:

		    Configura pruebas automatizadas, como pruebas unitarias, pruebas de integración y análisis estático de código, para garantizar la calidad del código antes de fusionarlo en la rama principal.

		    Además, automatiza los despliegues para facilitar la entrega continua.


		8. Utiliza Herramientas de Gestión de Proyectos:

		    Utiliza herramientas de gestión de proyectos, como tableros Kanban o sistemas de seguimiento de problemas, para organizar y priorizar el trabajo del equipo. 

		    Esto ayuda a mantener a todos en el mismo camino y a colaborar de manera eficiente.


		9. Fomenta la Retroalimentación Constructiva:

		    Fomenta un ambiente de retroalimentación constructiva donde los miembros del equipo se sientan cómodos compartiendo ideas y sugiriendo mejoras. 

		    La retroalimentación constructiva ayuda a mejorar la calidad del código y fomenta el crecimiento profesional.


		10. Documenta Decisiones y Procesos:

		    Documenta decisiones importantes, discusiones técnicas y procesos de desarrollo para que todos los miembros del equipo estén al tanto.

		    Esto facilita la colaboración y garantiza que todos estén en la misma página.

	
	Archivos: 

		1. Usa un archivo .gitignore:

		    Crea y utiliza un archivo .gitignore para especificar los archivos y directorios que deseas ignorar en el control de versiones de Git. 

		    Esto incluye archivos generados automáticamente, archivos de compilación y otros archivos no deseados.


		2. Divide Archivos en Unidades Lógicas:

		    Divide tu código en archivos y directorios que reflejen unidades lógicas y funcionales del proyecto. 

		    Esto facilita la navegación y la comprensión del código para ti y otros miembros del equipo.


		3. Evita Archivos Binarios en el Repositorio:

		    Evita incluir archivos binarios (como imágenes, videos o archivos compilados) en el repositorio de Git, especialmente si son grandes o cambian con frecuencia. 

		    En su lugar, utiliza sistemas de gestión de archivos binarios específicos si es necesario.


		4. Comparte Archivos de Configuración:

		    Comparte archivos de configuración importantes, como package.json en proyectos de Node.js o requirements.txt en proyectos de Python, para asegurarte de que todos los miembros del equipo tengan acceso a las mismas dependencias y configuraciones.


		5. Mantén Archivos de Documentación Actualizados:

		    Mantén archivos de documentación, como README.md, actualizados con información relevante sobre el proyecto, instrucciones de instalación, guías de contribución y cualquier otra información importante para los colaboradores y usuarios del proyecto.


		6. Usa Nombres de Archivos Descriptivos:

		    Utiliza nombres de archivos descriptivos y significativos que reflejen el propósito y el contenido del archivo. 

		    Esto facilita la comprensión del código y la navegación en el proyecto.


		7. Revisa Cambios en Archivos Grandes:

		    Antes de enviar cambios en archivos grandes, considera si es necesario dividir el archivo en unidades más pequeñas o utilizar técnicas de optimización para reducir el tamaño del archivo.


		8. Realiza Commits Atómicos:

		    Realiza commits atómicos que incluyan cambios relacionados y coherentes en archivos.

		    Evita realizar cambios no relacionados en el mismo commit para mantener un historial de cambios limpio y comprensible.


		9. Utiliza Ramas para Experimentos:

		    Si necesitas experimentar con cambios significativos en archivos, crea una nueva rama para trabajar en esos cambios y mantén la rama principal estable para el desarrollo continuo.


		10. Realiza Pruebas de Integración:

		    Antes de fusionar cambios en la rama principal, realiza pruebas de integración para asegurarte de que los cambios en los archivos funcionen correctamente con el resto del código base.


		11. Documenta Cambios Significativos:

		    Documenta cambios significativos en los archivos, especialmente aquellos que afectan la arquitectura, el rendimiento o la seguridad del proyecto.

		    Esto facilita la comprensión y la colaboración entre los miembros del equipo.



|| Gestión de archivos binarios
	
	Proceso de administrar y controlar archivos que contienen datos en un formato binario, es decir, datos representados en forma de secuencias de bits (0 y 1) que no son legibles directamente por humanos.


	Almacenamiento: 	

		Los archivos binarios pueden ocupar más espacio que los archivos de texto debido a su naturaleza de representar datos en forma de bits. 

		Por lo tanto, la gestión eficiente del almacenamiento es importante para asegurar que los archivos binarios se almacenen y administren correctamente.


    Seguimiento de Versiones: 

    	Al igual que con los archivos de texto, es esencial realizar un seguimiento de versiones de los archivos binarios para controlar los cambios realizados en ellos a lo largo del tiempo. 

    	Esto permite revertir cambios no deseados, restaurar versiones anteriores y mantener un historial de cambios.


    Control de Acceso: 

    	Dependiendo de la sensibilidad de los datos contenidos en los archivos binarios, puede ser necesario implementar medidas de control de acceso para garantizar que solo las personas autorizadas puedan acceder, modificar o eliminar dichos archivos.


    Integración con Herramientas de Desarrollo: 

    	Las herramientas de desarrollo y colaboración, como los sistemas de control de versiones (Git, SVN), los sistemas de gestión de proyectos y las herramientas de seguimiento de errores, deben ser compatibles con la gestión de archivos binarios para permitir una colaboración efectiva en proyectos de desarrollo de software.


    Dependencias y Relaciones: 

    	En muchos casos, los archivos binarios tienen dependencias entre sí o están relacionados con otros archivos en el proyecto. 

    	Es importante gestionar estas dependencias y relaciones para garantizar la integridad y coherencia del proyecto.


    Optimización de Rendimiento:

    	Dado que los archivos binarios pueden ser grandes y complejos, es importante optimizar el rendimiento de las operaciones de lectura y escritura para garantizar un acceso rápido y eficiente a los datos contenidos en ellos.


    Copias de Seguridad y Restauración: 

    	La gestión de archivos binarios también implica la realización regular de copias de seguridad de los datos para garantizar la recuperación en caso de pérdida o corrupción de archivos.


	Sistemas de gestión de archivos binarios: 

		Los archivos binarios contienen datos en un formato no legible directamente por humanos (a diferencia de los archivos de texto que se pueden leer y editar fácilmente).

		Se Utilizan sistemas de gestión principalmente en el desarrollo de software para gestionar recursos como imágenes, videos, archivos de audio, archivos ejecutables y otros tipos de archivos binarios.


		Gestión Eficiente de Archivos Binarios:

		    Los sistemas de gestión de archivos binarios están optimizados para manejar eficientemente archivos binarios de gran tamaño y complejidad, proporcionando capacidades de almacenamiento, seguimiento de cambios, versionado y colaboración.


		Control de Versiones Específico para Binarios:

		    A diferencia de los sistemas de control de versiones de texto como Git, que manejan eficazmente archivos de texto pero no son ideales para archivos binarios, los sistemas de gestión de archivos binarios están diseñados para gestionar eficientemente la versión de archivos binarios, manteniendo un historial de cambios y facilitando la colaboración en proyectos de desarrollo de software.


		Soporte para Diferentes Tipos de Binarios:

		    Estos sistemas pueden manejar una amplia variedad de tipos de archivos binarios, incluyendo imágenes, videos, archivos de audio, archivos ejecutables, archivos de documentos, archivos de base de datos y más.


		Funciones de Seguimiento de Cambios:

		    Proporcionan capacidades de seguimiento de cambios que permiten a los desarrolladores ver quién hizo qué cambios, cuándo se realizaron los cambios y revertir a versiones anteriores si es necesario.


		Gestión de Dependencias:

		    Algunos sistemas de gestión de archivos binarios ofrecen funcionalidades para gestionar dependencias entre archivos binarios, lo que facilita la gestión de proyectos complejos con múltiples dependencias.


		Integración con Herramientas de Desarrollo:

		    Se integran con herramientas de desarrollo populares, como IDEs (Entornos de Desarrollo Integrados) y sistemas de control de versiones, para proporcionar una experiencia de desarrollo más fluida y eficiente.


		Ejemplos de Sistemas de Gestión de Archivos Binarios:

		    Algunos ejemplos de sistemas de gestión de archivos binarios incluyen Apache Archiva, Artifactory, Nexus Repository Manager y Bintray.


		Uso en Industrias Específicas:

		    Los sistemas de gestión de archivos binarios son comunes en industrias como el desarrollo de software, la ingeniería de sistemas embebidos, la producción de videojuegos, la producción de medios digitales y la simulación.

|| Git Ignore
	
	Archivo de configuración especial utilizado por Git para especificar los archivos y directorios que deben ser ignorados y no incluidos en el control de versiones. 

	Esto es útil para evitar que archivos generados automáticamente, archivos compilados, dependencias de terceros y otros archivos no deseados se incluyan en el repositorio Git.


	Funcionamiento:

	    Especificación de Patrones:

	    	El archivo .gitignore utiliza patrones de coincidencia de rutas para especificar qué archivos y directorios deben ser ignorados por Git.


	    Formato Simple de Texto: 

	    	Es un archivo de texto plano que puedes crear y editar con cualquier editor de texto. 

	    	Cada línea del archivo representa un patrón de archivo o directorio a ser ignorado.


	    Comentarios: 

	    	Puedes incluir comentarios en el archivo precediendo la línea con el símbolo #.


	Ejemplos de Uso:

	    Ignorar Archivos Compilados:

	    	Por ejemplo, archivos ejecutables, archivos binarios y archivos generados durante el proceso de compilación (*.exe, *.o, *.class, etc.).


	    Ignorar Directorios de Dependencias: 

	    	Por ejemplo, directorios de dependencias de paquetes de gestores de dependencias (node_modules/, vendor/, packages/, etc.).


	    Ignorar Archivos de Configuración Locales: 

	    	Por ejemplo, archivos de configuración específicos de entornos locales (*.env, *.config, etc.).


	    Ignorar Archivos Temporales:

	    	Por ejemplo, archivos temporales y cachés (*.tmp, *.cache, etc.).


	Ubicación y Alcance:

	    El archivo .gitignore puede estar ubicado en el directorio raíz del repositorio Git o en cualquier subdirectorio del repositorio. 

	    Los patrones de ignora se aplican recursivamente a los archivos y directorios dentro del directorio donde se encuentra el archivo .gitignore y a sus subdirectorios.


	Gestión del Archivo .gitignore:

	    Es importante mantener el archivo .gitignore actualizado a medida que se agregan nuevos archivos y directorios al proyecto.

	    Puedes editar manualmente el archivo .gitignore o utilizar herramientas de generación de .gitignore disponibles en línea.

	    Aunque el archivo .gitignore puede ayudar a evitar la inclusión de archivos no deseados en el repositorio, es importante revisar los cambios antes de confirmarlos para asegurarse de que no se estén incluyendo inadvertidamente archivos importantes o sensibles.



|| Tableros Kanban

	Herramienta visual utilizada para gestionar y visualizar el flujo de trabajo en proyectos de desarrollo de software y en otros contextos. 

	Originario del sistema de producción Lean, el método Kanban se ha adaptado ampliamente en la gestión de proyectos ágiles y en el desarrollo de software.
	

	Características Principales:

	    Columnas: 

	    	Un tablero Kanban está dividido en columnas que representan diferentes etapas del flujo de trabajo, como "Por hacer", "En progreso" y "Hecho". 

	    	Cada columna puede tener una cantidad limitada de elementos que pueden estar en ella al mismo tiempo.


	    Tarjetas: 

	    	Las tarjetas representan unidades de trabajo individual, como tareas, historias de usuario o problemas. 

	    	Cada tarjeta se mueve a través del tablero de acuerdo con su estado y progreso.


	    Visualización: 

	    	La visualización clara y directa del tablero Kanban facilita la comprensión del estado del trabajo y la identificación de cuellos de botella o áreas problemáticas en el flujo de trabajo.


	    Limitación del Trabajo en Progreso (WIP): 

	    	Establecer límites en el número de tarjetas que pueden estar en cada columna ayuda a evitar la sobrecarga de trabajo y a mantener un flujo de trabajo equilibrado.


	Beneficios:

	    Visualización Clara: 

	    	Los tableros Kanban proporcionan una visualización clara del flujo de trabajo y del estado actual de las tareas en el proyecto.


	    Gestión de Prioridades:

	    	Permite a los equipos priorizar y gestionar el trabajo de manera efectiva al identificar y abordar las tareas más importantes primero.


	    Flexibilidad: 

	    	Los tableros Kanban son flexibles y se pueden adaptar fácilmente a diferentes tipos de proyectos y equipos.


	    Colaboración: 

	    	Facilita la colaboración entre los miembros del equipo al proporcionar una visión compartida del trabajo y permitir la asignación de tareas de manera transparente.


	    Mejora Continua: 

	    	Al identificar y abordar cuellos de botella en el flujo de trabajo, los equipos pueden mejorar continuamente sus procesos y aumentar su eficiencia.


	Implementación:

	    Los tableros Kanban se pueden implementar físicamente utilizando pizarras y tarjetas adhesivas, o de forma digital utilizando herramientas de gestión de proyectos como Trello, Jira, Asana, entre otras.

	    Los equipos pueden personalizar su tablero Kanban según sus necesidades específicas, agregando columnas adicionales, etiquetas, fechas de vencimiento y otros detalles relevantes.




|| Practica

	Git almacena versiones de nuestro código fuente. 
		
	Es utilizado en proyectos colaborativos. 
	
	Ofrece un historial de versiones para poder retrotraer el código por si algo sale mal. 
	
	Mantener varias versiones en paralelo y después poder unirlos. 
	
	 
	Comando git: 
		
		Muestra un resumen de las herramientas que posee. 
		
	Subcomandos: 
		
		Controlamos el programa por medio de otro comando además de git. 
		
		git subcomando o git -subcomando
		
	git init: 
		
		Crea un repo git 
		
		Es una carpeta que está oculta. 
		
		
		Copias de seguridad: 
			
			Clonar un repo.
			
			Almacenarlo en la nube de GitHub o GitLab, etc. 
			
			O Sincronizarlo directamente con estos servicios. 
			
	
	git status: 
		
		Nos muestra información como: 
		
		rama/branch
		
		rama actualizada
		
		cambios/commit en el repo git. 
		
		modificaciones no registrada/untracked
		

	Commit: 
	
		La idea es almacenar los cambios concretos que hagamos en el repo. 
		
		
		git add: 
		
			Registra los cambios. 
			
		
		De untracked a staged: 
			
			git add 'nombre del archivo'
			
			
		Cambios a ser confirmados/changes to committed: 
		

		git commit: 
		
			Abre un espacio para escribir. 
			
			Debemos describir significativamente que contiene el cambio. 
			
			Nos mostrará en que rama se hizo el commit
			
			También el número. 
		
		
			git status: 
			
				Si no hay nada, va a decir que el repo está limpio. 
				
				

	Working Directory: 
		
		
		git log: 
			
			Muestra una lista de commits
			
			Muestra el número de hash sha1
			
			sha1 es un algoritmo de suma de comprobación. 
			
			Crea un hash para el contenido de cada commit. 
			
			Cada commit tiene un identificador distinto. 
			
			Por cuestiones de seguridad, el hash se genera a partir del mensaje del cambio y los archivos. 
			
			Si alguien quiere intenta modificar un archivo, tendría que cambiar el hash. 
			
			
		git status: 
			
			Puede que nos marque el working directory. 
			
			Es la carpeta donde podemos hacer modificaciones. 
			
			Si nos dice que está limpio es porque contiene los archivos ya creados. 
			
			
		ls: 
		
			Podemos comprobar los archivos del directorio. 
			
			
		Si hacemos cambios, git status lo detectará. 
		
		
		git diff: 
			
			Podemos ver en detalle lo que hemos modificado. 
			
			Lo que está y lo que no está en el Staged. 
			
			Las lineas verdas son las agregadas. 
			
			Las lineas rojas las eliminadas. 
			
		
		git add . 
			
			Metemos los cambios de todos los archivos. 
			
			
		git add 'nombre del archivo'
		
			Mete los cambios por separado. 
			
			
		




















