# factory-methoad1
metodo fabrica ejemplos

ejemplo de personajes 

void main() {
  Fabrica fabrica =  Fabrica();
  
  Personaje personaje = fabrica.obtenerpersonaje("Mario");
  personaje.saltar;
  personaje.correr;
}
class Fabrica {
  Personaje obtenerpersonaje(tipo){
    if (tipo == "Mario"){
      return Mario();
    }else if (tipo == "Goku"){
      return Goku();
    }
    else{
      return Superman();
    }
  }
}
abstract class Personaje{
  void saltar();
  void correr();
}

class Mario implements Personaje{
  @override
  void saltar(){
    print ("Mario salta");
  }
  
  void correr(){
    print ("Mario corre");
  }
}

class Goku implements Personaje{
  @override
  void saltar(){
    print("Goku salata");
  }
  void correr(){
    print("Goku corre");
  }
}
class Superman implements Personaje{
  @override
  void saltar(){
    print("Superman salata");
  }
  void correr(){
    print("Superman corre");
  }
}
