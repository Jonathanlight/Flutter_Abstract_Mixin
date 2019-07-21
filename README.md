# Flutter_Abstract_Mixin
Use Class Abstract &amp; Mixin with Dart

```

mixin DevSymfony {
  void codingSymfony() {
    print('coding');
  }  
}
​
mixin DevLaravel {
  void codingLaravel() {
    print('Laravel coding');
  }  
}
​
mixin DevDjango {
  void codingDjango() {
    print('Django coding');
  }  
}
​
abstract class Develop {
  void makeDevelop() {
    print('i am develop');
  }
}
​
abstract class DevPhp extends Develop with DevSymfony, DevLaravel {
  void makePhp() {
    print('i am dev PHP');
  }
}
​
class HtmlCssDevelop extends DevPhp {
  void makeFrontEnd() {
    makeDevelop();
    codingSymfony();
    makePhp();
    print('css & html');
  }
}
​
abstract class ApiDev with DevSymfony, DevDjango{
  void makeAPI() {
    print('i work with API PLATEFORME');
  }
}
​
class Experience extends ApiDev {
  void doAngular(){
    makeAPI();
    codingSymfony();
    print('i work with angular');
  }
}
​
void main() {
  Experience().doAngular();
}
```
