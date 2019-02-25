
#Parte de la tarea 2.
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

  