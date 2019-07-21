# Flutter_Abstract_Mixin
Use Class Abstract &amp; Mixin with Dart
https://medium.com/flutter-community/dart-what-are-mixins-3a72344011f3

```

mixin DevSymfony {
  void codingSymfony() {
    print('Symfony coding');
  }  
}

mixin DevLaravel {
  void codingLaravel() {
    print('Laravel coding');
  }  
}

mixin DevDjango {
  void codingDjango() {
    print('Django coding');
  }  
}

abstract class Develop {
  void makeDevelop() {
    print('i am develop');
  }
}


abstract class DevPhp extends Develop with DevSymfony, DevLaravel {
  void makePhp() {
    print('i am dev PHP');
  }
}

class HtmlCssDevelop extends DevPhp {
  void makeFrontEnd() {
    makeDevelop();
    codingSymfony();
    makePhp();
    print('css & html');
  }
}

mixin Ide on ApiDev {
  void phpStorm() {
    print('phpStorm');
    makeAPI();
  }  
}

abstract class ApiDev with DevSymfony {
  void makeAPI() {
    print('i work with API PLATEFORME');
  }
}

class Experience extends ApiDev {
  void doAngular(){
    makeAPI();
    codingSymfony();
    print('i work with angular');
  }
}

abstract class Super {
  void method() {
    print("Super");
  }
}

class MySuper extends Super {
  void method() {
    print("MySuper");
  }
}

mixin Mixin on Super {
  void method() {
    super.method();
    print("Sub");
  }
}

class Client extends MySuper with Mixin {}

void main() {
  Client().method();
  Experience().doAngular();
  Experience().codingSymfony();
}
```
