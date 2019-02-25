#Tarea 2.
---

###2.1 Declaración de clases: atributos, métodos, encapsulamiento.
Básicamente lo que trata el tema, es  como se usa la programación orientada a objetos o al menos lo mas básico. Al estar programando en este tipo de lenguajes,
cualquier programa que nosotros estemos creando, se dividen en partes llamadas clases, en las cuales el conjunto de todas esas clases, se crea el objeto principal del programa (como por ejemplo "bicicleta" se dividen en partes llamadas clases como: clase llanta, clase, pedal, etc).

Todas esas clases de una forma u otra forma interactúan entre si, con mecanismos que los ayudan con tal fin, ya sea con herencias, dejando el método publico o por medio de Main.

La herencia sirve para que una clase o varias clases que heredan de otra, puedan usar variables de otras clases (padre a hijo), métodos o asta sobrecargas, si así lo requiriera.
Pero la clase padre no puede tomar los aspectos que tenga sus clases hijas.

El encapsulamiento nos sirve para que el proyecto en desarrollo este protegido, sirve para que el usuario solo vea lo que le permitas ver, pero dependiendo del el nivel de encapsulamiento, sera su nivel de protección, por eso debe de tener un buen encapsulamiento el programa. 

### 2.2 Instanciación de una clase.
El operador new, nos sirve para crear objetos e invocar constructores, también se utiliza para crear instancias de tipos anónimos. Anteriormente en las clases ya hemos usado el operador new, para crear instancias de las clases en Main, pero al usarlo de forma secundaria también se invoca al constructor, por lo que para evitar un error del sistema, cuando nosotros no hemos creado el constructor de la clase, el mismo programa crea uno de referencia, pero sin presentar cambio alguna hacia nuestro programa en cuestión.     
###  2.4 Métodos: declaración, mensajes, paso de parámetros, retorno de valores.
- **Parámetros:** Los parámetros es una forma de intercambiar información en un método de forma fácil. 

- **Out:** Puedes utilizar Out como un modificador de parámetro, que le permite pasar un argumento a un método mediante una referencia en lugar de mediante un valor.
En declaraciones de parámetro de tipo genérico para interfaces y delegados, que especifica que un parámetro de tipo es covariante.

- **Ref:** Ref sirve para enviarte al lugar donde se saco dicha referencia, también sirve para darte una referencia de como se hace un método en especifico y a veces asta dándole click automáticamente te da una buena forma de como se hace dicho método.
    
###2.5 Constructores y destructores: declaración, uso y aplicaciones.
- Constructor:
Los constructores son métodos de clase que se ejecutan cuando se crea un objeto de un tipo determinado. Los constructores tienen el mismo nombre que la clase y, normalmente, inicializan los miembros de datos del nuevo objeto.

- **Destructor:**
Un destructor se podría decir que es lo contrario al constructor, como su nombre lo indica "destruye al objeto", pero lo que se hace realmente no es como uno se lo imagina, lo que hace es cambiar el contenido por un vació (""), de esa forma el programa lo tomaría como si no tuviera nada.  

###2.6 Sobrecarga de métodos. 
La sobrecarga, sirve para clonar un contenido de un método o constructor, pero con diferentes variantes y al momento de llamarlo por program Main, se invoca aquel que se adapte, dependiendo si tiene parámetros o con diferentes variantes.

(2.3 Referencia al objeto actual. y 2.7 Sobrecarga de operadores: Concepto y utilidad, operadores unarios y binarios)

###  2.3 Referencia al objeto actual.  
---
    class persona
    {
        private string nombre;
        private int edad;
        public persona(string nombre, int edad)
        {
            this.nombre = nombre;
            this.edad = edad;
        }
        public void Imprime()
        {
            Console.WriteLine("Se llama: {0} y su edad es: {1}", nombre, edad);
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            persona hola = new persona("Jose de jesus", 21);
            hola.Imprime();
            Console.ReadKey();
        }
    }

###  2.7 Sobrecarga de operadores: Concepto y utilidad, operadores unarios y binarios.
---
    class Dato
    {
        private double valor;
        private string color;
        private string estilo;
        public string Estilo 
        {
            get
            {
                return estilo;
            }
            set
            {
                estilo = value;
            }
        }
        public Dato()
        {
            valor = 27.5;
            color = "Azul";
        }
        public Dato(double valor, string color)
        {
            this.valor = valor;
            this.color = color;
        }
        public void Imprime()
        {
            Console.WriteLine("El valor es {0} y su color es {1}", valor, color);
        }
        public void Imprime(string hola)
        {
            Console.WriteLine(hola + " " + estilo);
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            Dato salida = new Dato();
            Dato entrada = new Dato(15.8, "Verde");
            entrada.Estilo = "Bueno";
            salida.Estilo = "Malo";
            entrada.Imprime();
            salida.Imprime("esto es ");
            Console.ReadKey();
        }
    }