# BMPerfomance-Full

1). For a project with a framework like: ( Symfony ) you need to install NeatBeans 8.2 Ide or Netbeans 11.0 or whatever !


2). For install Neatbeans you need to install: [ Cygwin Terminal ] for Terminal in NetBeans ! 


3). Install [ Cygwin ] from here : https://www.cygwin.com/  - Download last version ! 


4). Install ( NetBeans 8.2 ) - You can install a new version if you want, but now i use NetBeans 8.2 Ide : https://netbeans.org/downloads/8.2/


5). NetBeans IDE Download Bundles - Download version with all included ( 221 mb ). 


6). Install [ JDK 8u111 ] from here : https://www.oracle.com/technetwork/java/javase/downloads/jdk-netbeans-jsp-3413139-esa.html. 

6.1). Click on button : Accept License Agreement. 

6.2). If you have Windows with 64 bit DOWNLOAD this version : jdk-8u111-nb-8_2-windows-x64.exe / 



--------------------------------------------------------------


7). For next steps you need to already have installed Cygwin Terminal and NetBeans on your PC !


8). Now OPEN NetBeans and check for ICON with : NEW PROJECT / or write on your keyboard : Ctrl + Shift + N . 


9). Chose Project : Php Application ! / Next > / Chose a project name / example : BMProject ; MySite ; or whatever do you like... / 




--------------------------------------------------------------


10). Now go to : Documents\NetBeansProjects\ 

And CREATE A NEW FOLDER with your PROJECT-NAME ...



--------------------------------------------------------------


11). For my Style i like to do like this => 

=> Now you need to have 2 Folders in your Parent Folder ! 

For example my project name is : BMPerfomance. / 

And in my interior folder i have 2 folders - 1 is BMPerfomance and other one is : Default_BMPerfomance. / 



--------------------------------------------------------------


12). For next steps my example is : 

     Set =>  Project Name : BMPerfomance			
     Set =>  Browse for : C:\Users\L30\Documents\NetBeansProjects\BMPerfomance\
     Set =>  Sources Folder : C:\Users\L30\Documents\NetBeansProjects\BMPerfomance\
     Set =>  Php Version : Php 7.0 
     Set =>  Default Enconding : UTF-8


13). Next > 
      
     Set =>  Run As : Local Web Site (running on local web server)
     Set =>  Project Url : http://localhost/BMPerfomance/ 


14). Next > 

     Don`t set the framework now ! 

     Do it mannually ! 


15). Next > 


16). Finish !



--------------------------------------------------------------


17). Now in NetBeans Project i have like this : 
   
- BMPerfomance
-> Source Files => BMPerfomance folder 
                => Default_BMPerfomance folder 
-> Include Path
-> Remote Files / ... 



--------------------------------------------------------------


18). Right click on my inside folder : BMPerfomance => Tools -> Open in Terminal ! 

For my example in terminal i have like this : L30@L30-PC /cygdrive/c/Users/L30/Documents/NetBeansProjects/BMPerfomance/BMPerfomance 



--------------------------------------------------------------


19). For next steps you need to install Composer ! 

[ Type this in your NetBeans Terminal ! ] 

php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'a5c698ffe4b8e849a443b120cd5ba38043260d5c4023dbf93e1558871f1f07f58274fc6f4c93bcfd858c6bd0775cd8d1') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"



--------------------------------------------------------------


20). Now you have installed in my BMPerfomance folder : composer.phar

[ Type for more commands informations : php composer.phar ! 
 
- Now Go to : https://getcomposer.org/ and install Composer ! 



--------------------------------------------------------------


21). Install Symfony now : https://symfony.com/download 

- Right-click on BMPerfomance from : Source Files and then => 

- I type in terminal like this : [ composer create-project symfony/website-skeleton BMPerfomance ]  

- Now just wait to install the files ! 



--------------------------------------------------------------


22). Now execute this command in terminal [ Right-click on your child folder like this : L30@L30-PC /cygdrive/c/Users/L30/Documents/NetBeansProjects/BMPerfomance/BMPerfomance. <= In Terminal need to look like this ] 

Link for command : https://symfony.com/doc/current/bundles/SymfonyMakerBundle/index.html / Command : composer require symfony/maker-bundle --dev 



--------------------------------------------------------------


23). This command also : composer require doctrine/doctrine-bundle / From here : https://symfony.com/doc/current/bundles/DoctrineBundle/installation.html / 


--------------------------------------------------------------


24). Now this command : composer require symfony/orm-pack / And wait for files to be installed / You can check this command : https://symfony.com/doc/current/doctrine.html



--------------------------------------------------------------


25). Now this command also : composer require --dev symfony/maker-bundle / You can find it here : https://symfony.com/doc/current/bundles/DoctrineBundle/installation.html



--------------------------------------------------------------


26). Execute this command -> Is important : composer require symfony/dotenv / 



--------------------------------------------------------------


27). This command is very important for your project ! / Command : composer require symfony/apache-pack  / The package symfony/apache-pack installs a .htaccess file in the public directory that contains the rewrite rules.

Link : https://thecodingmachine.io/building-a-single-page-application-with-symfony-4-and-vuejs 



--------------------------------------------------------------


28). New command for finding ERRROS : composer require --dev phpstan/phpstan / PHPStan focuses on finding errors in your code without actually running it. It catches whole classes of bugs even before you write tests for the code.

Link for Command : https://thecodingmachine.io/building-a-single-page-application-with-symfony-4-and-vuejs 



--------------------------------------------------------------


29). Very important Commands for Doctrine => 

1). composer require doctrine/doctrine-migrations-bundle "^1.0"

2). composer require friendsofsymfony/rest-bundle

3). composer require --dev doctrine/doctrine-fixtures-bundle

--------------------------------------------------------------

4). php bin/console doctrine:migrations:diff /.../ Don`t use this command now !
 
5). php bin/console doctrine:migrations:migrate /.../ Don`t use this command now !

6). php bin/console doctrine:fixtures:load /.../ Don`t use this command now !

Link for commands : https://thecodingmachine.io/building-a-single-page-application-with-symfony-4-and-vuejs



--------------------------------------------------------------


30). Command for Doctrine also : php vendor/bin/doctrine / You need to register your applications EntityManager to the console tool to make use of the tasks by creating a cli-config.php file with the following content: 

Link for command : https://www.doctrine-project.org/projects/doctrine-orm/en/2.6/reference/configuration.html 



--------------------------------------------------------------


31). Type this 2 commands : 

1). php bin/console config:dump-reference doctrine /  

For : displays the default config values defined by Symfony


2). php bin/console debug:config doctrine / 

For : displays the actual config values used by your application.


--------------------------------------------------------------


32). Next command for Twig Template : php bin/console debug:twig

Twig comes with a long list of tags, filters and functions that are available by default. 

Run the following command to list them all.

Link : https://symfony.com/doc/current/templating.html



--------------------------------------------------------------


33). Command : php bin/console debug:autowiring 

What other services can you type-hint? To see them, use the debug:autowiring console command ! 

Link : https://symfony.com/doc/current/controller.html



--------------------------------------------------------------


34). Command : composer require symfony/asset

A). Templates also commonly refer to images, JavaScript, stylesheets and other assets. 

You could hard-code the web path to these assets (e.g. /images/logo.png), but Symfony provides a more dynamic option via the asset() Twig function.

To use this function, install the asset package !

--------------------------------------------------------------

B). You can now use the asset() function:

<img src="{{ asset('images/logo.png') }}" alt="Symfony!"/>

<link href="{{ asset('css/blog.css') }}" rel="stylesheet"/>


Link : https://symfony.com/doc/current/templating.html


--------------------------------------------------------------


35). Command : php bin/console list make

This bundle provides several commands under the make: namespace. List them all executing this command.



--------------------------------------------------------------


36). Type this commands for: controllers, entitys, commands... etc

commands : 1). php bin/console make:controller --help
           
           2). php bin/console make:entity --help

           3). 1). php bin/console make:command --help



--------------------------------------------------------------


37). Command : php bin/console make:controller 

Choose a name for your controller class (e.g. AgreeablePuppyController) : 
> BrandNewController

created: src/Controller/BrandNewController.php
created: templates/brandnew/index.html.twig


- To save time, you can install Symfony Maker and tell Symfony to generate a new controller class.

Link : https://symfony.com/doc/current/controller.html



--------------------------------------------------------------


38). Command : php bin/console make:crud Product

created: src/Controller/ProductController.php
created: src/Form/ProductType.php
created: templates/product/_delete_form.html.twig
created: templates/product/_form.html.twig
created: templates/product/edit.html.twig
created: templates/product/index.html.twig
created: templates/product/new.html.twig
created: templates/product/show.html.twig


If you want to generate an entire CRUD from a Doctrine entity !

Link : https://symfony.com/doc/current/controller.html


--------------------------------------------------------------


39). OTHER COMMANDS YOU CAN FIND YOURSELF WITH THIS COMMAND : php bin/console -list 

OR THIS COMMAND : php bin/console make: 


--------------------------------------------------------------


LINKS : 



https://getcomposer.org/

https://getcomposer.org/download/

https://symfony.com/doc/current/setup.html#installing-packages

https://symfony.com/doc/current/bundles/SymfonyMakerBundle/index.html

https://symfony.com/doc/current/doctrine.html

https://symfony.com/doc/current/bundles/DoctrineBundle/installation.html

https://symfony.com/doc/current/doctrine/registration_form.html?fbclid=IwAR1uBOeVxsWa4x19jiCYMMZA9eKrBpjuHgBA1vJFtJv8x6Xks70Nl_WwINQ#before-you-get-started

https://symfony.com/download

https://twig.symfony.com/doc/2.x/intro.html?fbclid=IwAR1oMfeafbfl8j-OrAxLbwwlwewUP-hk33Q4i9aXxcc9QtRA91wSQpgNAi0

https://symfony.com/doc/current/bundles/SensioGeneratorBundle/commands/generate_controller.html

https://thecodingmachine.io/building-a-single-page-application-with-symfony-4-and-vuejs

https://symfony.com/doc/current/reference/configuration/doctrine.html

https://www.doctrine-project.org/projects/doctrine-orm/en/2.6/reference/configuration.html

https://symfony.com/doc/current/templating.html

https://symfony.com/doc/current/controller.html

https://symfony.com/doc/current/bundles/SymfonyMakerBundle/index.html

https://symfony.com/doc/current/console.html

https://symfony.com/doc/2.6/cookbook/console/console_command.html

https://symfony.com/doc/current/best_practices/controllers.html

https://ourcodeworld.com/articles/read/847/top-7-best-open-source-php-template-engines

https://github.com/BogdanMarianC/console

https://symfony.com/doc/current/components/console.html

https://vfac.fr/blog/how-to-install-easyadmin-with-fosuserbundle-in-symfony-4

https://vfac.fr/blog/how-to-use-doctrine-mongo-db-with-symfony-4



--------------------------------------------------------------



LINKS :

https://getcomposer.org/

https://getcomposer.org/download/

https://symfony.com/doc/current/setup.html#installing-packages

https://symfony.com/doc/current/bundles/SymfonyMakerBundle/index.html

https://symfony.com/doc/current/doctrine.html

https://symfony.com/doc/current/bundles/DoctrineBundle/installation.html

https://symfony.com/doc/current/doctrine/registration_form.html?fbclid=IwAR1uBOeVxsWa4x19jiCYMMZA9eKrBpjuHgBA1vJFtJv8x6Xks70Nl_WwINQ#before-you-get-started

https://symfony.com/download

https://twig.symfony.com/doc/2.x/intro.html?fbclid=IwAR1oMfeafbfl8j-OrAxLbwwlwewUP-hk33Q4i9aXxcc9QtRA91wSQpgNAi0

https://symfony.com/doc/current/bundles/SensioGeneratorBundle/commands/generate_controller.html

https://thecodingmachine.io/building-a-single-page-application-with-symfony-4-and-vuejs

https://symfony.com/doc/current/reference/configuration/doctrine.html

https://www.doctrine-project.org/projects/doctrine-orm/en/2.6/reference/configuration.html

https://symfony.com/doc/current/templating.html

https://symfony.com/doc/current/controller.html

https://symfony.com/doc/current/bundles/SymfonyMakerBundle/index.html

https://symfony.com/doc/current/console.html

https://symfony.com/doc/2.6/cookbook/console/console_command.html

https://symfony.com/doc/current/best_practices/controllers.html

https://ourcodeworld.com/articles/read/847/top-7-best-open-source-php-template-engines

https://github.com/BogdanMarianC/console

https://symfony.com/doc/current/components/console.html

https://vfac.fr/blog/how-to-install-easyadmin-with-fosuserbundle-in-symfony-4

https://vfac.fr/blog/how-to-use-doctrine-mongo-db-with-symfony-4



--------------------------------------------------------------



VIDEO LINKS :

https://symfonycasts.com/tracks/symfony

https://symfonycasts.com/screencast/symfony/setup

https://symfonycasts.com/screencast/symfony-fundamentals/config-bundle

https://symfonycasts.com/screencast/symfony-doctrine/saving-entities

https://symfonycasts.com/screencast/doctrine-relations/comment-entity

https://symfonycasts.com/screencast/symfony-security/make-user

https://symfonycasts.com/screencast/symfony-forms/form-type-class

https://codereviewvideos.com/course/symfony-4-beginners-tutorial/video/getting-started-with-symfony-4

https://vfac.fr/blog/how-to-install-easyadmin-with-fosuserbundle-in-symfony-4

https://vfac.fr/blog/how-to-use-doctrine-mongo-db-with-symfony-4



--------------------------------------------------------------


OTHER LINKS :

https://learn.freecodecamp.org/?fbclid=IwAR31nruZNfWWRDQDSys4NhiBJh5GdX2-jKOKGjfelF5DKOGc0uok-1UaBUA

https://codereviewvideos.com/course/symfony-4-beginners-tutorial/video/symfony-make-controller

https://github.com/doctrine/DoctrineBundle/issues/746

https://stackoverflow.com/questions/55687722/an-exception-occurred-in-driver-sqlstatehy000-1045-access-denied-for-user

https://github.com/miezuit?tab=repositories&fbclid=IwAR3Upy8tMxCraPSeyTIXbbW1Su7Pw60c5DktRQECTpkMy92zDLp2FaPVkuo

https://github.com/doctrine/DoctrineBundle/issues/746

https://symfony.com/doc/current/setup.html

https://symfony.com/doc/current/page_creation.html

https://symfony.com/doc/current/doctrine/registration_form.html?fbclid=IwAR2GPVJU48QCyWz3-8IbAzt9PHAG8faLfIbrh0-YJTMxgijqLUgm8MvR_BE#before-you-get-started

https://twig.symfony.com/doc/2.x/intro.html?fbclid=IwAR3FpYjku9wpOT5Si56DD47WQeC4rP7hBzdkWAKY5oTPQnpKZK9bnL9DppY


