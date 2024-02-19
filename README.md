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

ejemplo base de datos 

void main(){
  Fabrica fabrica = Fabrica();
  Bd bd = fabrica.conexion(1);
  bd.conectar;
  bd.desconectar;
}

class Fabrica{
  Bd conexion (int tipo){
    if (tipo == 1){
      return Mysql();
    }else{
      return Oracle();
    }
    
  }
}
abstract class Bd {
  void conectar();
  void desconectar();
}

class Mysql implements Bd {
  @override
  void conectar(){
    print ("conectar con mysql");
  }
  void desconectar(){
    print ("desconetar con mysql");
  }
}

class Oracle implements Bd {
  @override
  void conectar(){
    print ("conectar con oracle");
  }
  void desconectar(){
    print ("desconectar con oracle");
  }
}

ejemplo de data 

void main() {
  Fabrica fabrica = Fabrica();
  Data d = fabrica.getdata(2);
  d.data;
}
class Fabrica{
  Data getdata (int tipo){
    if (tipo == 1){
      return Resqres();
    }else{
      return Mypokeapi();
    }
  }
}
abstract class Data{
  void data();
}

class Resqres implements Data{
  @override
  void data(){
    print("uste esta usando reqres");
  }
}
class Mypokeapi implements Data{
  @override
  void data(){
    print("uste esta usando mypokeapi");
  }
}
