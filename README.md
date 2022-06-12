### Тестовое задание Ай-Новус

**Проблемы, с которыми столкнулась при создании тестового проекта**

1. В документации указан файл `pom.xml` с необходимыми зависимостями, однако для сборки приложения необходимо было добавить дополнительную зависимость `lombok`. Без данной зависимости при сборке пакета выходила ошибка `Fatal error compiling: java.lang.IllegalAccessError: class lombok.javac.apt.LombokProcessor (in unnamed module @0x753aca85) cannot access class com.sun.tools.javac.processing.JavacProcessingEnvironment (in module jdk.compiler) because module jdk.compiler does not export com.sun.tools.javac.processing to unnamed module @0x753aca85`
2. В документации указано, что для запуска проекта необходимо установить OpenJDK 11+. При этом при использовании OpenJDK версии 18.0.1.1 выходила ошибка `java.lang.NoSuchMethodException: no such method: sun.misc.Unsafe.defineAnonymousClass(Class,byte[],Object[])Class/invokeVirtual`. Проект запустился только при использовании версии 16.0.1
   