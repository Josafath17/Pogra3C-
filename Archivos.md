using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.IO;


namespace Calculadora
{
    class Program
    {
        static void Main(string[] args)
        {
            bool salir = false;



            while (!salir)
            {
                String line;
                try
                {

                    Console.WriteLine("Bienvenido a La Carculadora");
                    Console.WriteLine("1. Suma de 2 numeros Enteros");
                    Console.WriteLine("2. Resta de 2 numeros enteros");
                    Console.WriteLine("3. Multiplicar de 2 numeros enteros");
                    Console.WriteLine("4. Dividir de 2 numeros enteros");
                    Console.WriteLine("5. Potencia de 1 numeros enteros");
                    Console.WriteLine("6. Salir");
                    Console.WriteLine("Elige una de las opciones");
                    int opcion = Convert.ToInt32(Console.ReadLine());

                    switch (opcion)
                    {

                        case 1:
                            Console.WriteLine("La Funcionalidad es Sumar 2 numeros Enteros!");

                            int numero1, numero2, resultado;
                            Console.WriteLine("Ingrese Primer número: ");
                            numero1 = int.Parse(Console.ReadLine());
                            Console.WriteLine("Ingrese Segundo número: ");
                            numero2 = int.Parse(Console.ReadLine());
                            resultado = numero1 + numero2;
                            Console.WriteLine("El resultados es: " + resultado);
                            
                            GuardarArchivos(numero1 + " +" + numero2 + "= " + resultado + " ");


                            break;
                        case 2:
                            Console.WriteLine("La Funcionalidad Resta 2 numeros Enteros!");
                            Console.WriteLine("Ingrese Primer número: ");
                            numero1 = int.Parse(Console.ReadLine());
                            Console.WriteLine("Ingrese Segundo número: ");
                            numero2 = int.Parse(Console.ReadLine());
                            resultado = numero1 - numero2;
                            Console.WriteLine("El resultados es: " + resultado);
                            GuardarArchivos(numero1 + " -" + numero2 + "= " + resultado + " ");

                            break;
                        case 3:
                            Console.WriteLine("La Funcionalidad Multiplicar 2 numeros Enteros!");

                            Console.WriteLine("Ingrese Primer número: ");
                            numero1 = int.Parse(Console.ReadLine());
                            Console.WriteLine("Ingrese Segundo número: ");
                            numero2 = int.Parse(Console.ReadLine());
                            resultado = numero1 * numero2;
                            Console.WriteLine("El resultados es: " + resultado);
                            GuardarArchivos(numero1 + " *" + numero2 + "= " + resultado + " ");

                            break;
                        case 4:

                            Console.WriteLine("La Funcionalidad Dividir 2 numeros Enteros!");

                            Console.WriteLine("Ingrese Primer número: ");
                            numero1 = int.Parse(Console.ReadLine());
                            Console.WriteLine("Ingrese Segundo número: ");
                            numero2 = int.Parse(Console.ReadLine());
                            resultado = numero1 / numero2;
                            Console.WriteLine("El resultados es: " + resultado);
                            GuardarArchivos(numero1 + "/" + numero2 + "= " + resultado + " ");
                            break;
                        case 5:
                            Console.WriteLine("La Funcionalidad Elevar 1 numero Enteros!");

                            double numero, potencia, elevado;
                            Console.WriteLine("Ingrese Numero: ");
                            numero = int.Parse(Console.ReadLine());
                            Console.WriteLine("Ingrese la Potencia:");
                            potencia = int.Parse(Console.ReadLine());

                            elevado = Math.Pow(numero, potencia);
                            Console.WriteLine(string.Format("{0} elevado a la potencia {1} es {2}", numero, potencia, elevado));
                            GuardarArchivos(numero + "^" + potencia + "= " + elevado + " ");

                            break;

                        case 6:
                            Console.WriteLine("Has elegido salir de la aplicación");
                            salir = true;
                            break;
                        default:
                            Console.WriteLine("Elige una opcion entre 1 y 6");
                            break;
                    }

                }

                catch (FormatException e)
                {
                    Console.WriteLine(e.Message);
                }
                Console.ReadLine();
                Console.Clear();
            }

        }
        private static void GuardarArchivos(string fs)
        {

            StreamWriter archivo = new StreamWriter("C:\\Users\\Estudiante.COMSSC2342\\source\\repos\\Calculadora\\Calculadora\\Calculador.txt");
            archivo.WriteLine(fs);
            archivo.Close();

        }
    }
}
