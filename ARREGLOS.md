# Pogra3C-
Programa 3 , segundo cuatri C#

namespace Restaurante_Menu
{
    internal class Platillo

    {
       
            public string nombre;
            public int precio;
            public Platillo(string nombre, int precio)
            {
                this.nombre = nombre;
                this.precio = precio;
            }

            public override string ToString()
            {
                return "Nombre de platillo " + this.nombre + " y Precio " + this.precio;
            }
           
        }
        
        
        
        
        parte 2
        namespace Restaurante_Menu
{
 


class Program

    {
        static void recorrerArreglo(Platillo[] Menu)
        {
            foreach (var Platillo in Menu)
            {
                Console.WriteLine("Platillo " + Platillo);
               // Platillo.ToString();
            }
        }


        static void Main(string[] args)
        {

            Platillo[] Menu = { new Platillo("Arroz con Pollo", 3000), new Platillo("María", 24) };
            recorrerArreglo(Menu);

            bool salir = false;




            while (!salir)
            {
                try
                {


                    Console.WriteLine("Menu Restaurante la Ezquina");
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

                        case 6:
                            Console.WriteLine("Has elegido salir de la aplicación");
                            salir = true;
                            break;
                    }
                     
                }
                catch (FormatException e)
                {

                }
}
        }
    }
}

