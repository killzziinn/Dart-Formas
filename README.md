abstract class Forma {
 
  void desenhar();
  
  double area();
}


class Circulo extends Forma {
  double raio;

  Circulo(this.raio);

  void desenhar() {
    print("Desenhando um círculo com raio $raio.");
  }

  double area() {
    return 3.14159 * raio * raio;
  }
}

class Retangulo extends Forma {
  double comprimento;
  double altura;

  Retangulo(this.comprimento, this.altura);

  void desenhar() {
    print("Desenhando um retângulo com largura $comprimento e altura $altura.");
  }

  double area() {
    return comprimento * altura;
  }
}

class Triangulo extends Forma {
  double base;
  double altura;

  Triangulo(this.base, this.altura);

  
  void desenhar() {
    print("Desenhando um triângulo com base $base e altura $altura.");
  }

  double area() {
    return (base * altura) / 2;
  }
}

void main() {
  
  Forma circulo = Circulo(5.0);
  Forma retangulo = Retangulo(10.0, 20.0);
  Forma triangulo = Triangulo(6.0, 8.0);

  circulo.desenhar(); // 
  print("Área do círculo: ${circulo.area()}"); 

  retangulo.desenhar(); 
  print("Área do retângulo: ${retangulo.area()}"); 

  triangulo.desenhar(); // 
  print("Área do triângulo: ${triangulo.area()}"); 
}
