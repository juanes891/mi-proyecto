# mi-proyecto
// autor: Juan David Morales 
// grupo:213022_66
// programa:ingenieria de sistemas
using System;

partial class Program
{
    static void Main(string[] args)
    {
        // Variables
        int nacimientosMensuales;
        int muertesMensuales, sobrevivenMensualmente;
        int muertesAnuales, sobrevivenAnualmente;

        // Entrada: Número de nacimientos mensuales
        Console.Write("Ingrese la cantidad de niños que nacen mensualmente: ");
        nacimientosMensuales = int.Parse(Console.ReadLine());

        // Cálculos
        muertesMensuales = (nacimientosMensuales * 2) / 10; // El 20% fallece
        sobrevivenMensualmente = nacimientosMensuales - muertesMensuales;

        muertesAnuales = muertesMensuales * 12; // Total anual
        sobrevivenAnualmente = sobrevivenMensualmente * 12; // Total anual

        // Salida de resultados
        Console.WriteLine("\nResultados:");
        Console.WriteLine($"Niños que mueren mensualmente: {muertesMensuales}");
        Console.WriteLine($"Niños que sobreviven mensualmente: {sobrevivenMensualmente}");
        Console.WriteLine($"Niños que sobreviven anualmente: {sobrevivenAnualmente}");
        Console.WriteLine($"Niños que mueren anualmente: {muertesAnuales}");

        // Verificar estado de alerta
        if (muertesAnuales > 100)
        {
            Console.WriteLine("Estado de alerta: Sí, mueren más de 100 niños anualmente.");
        }
        else
        {
            Console.WriteLine("Estado de alerta: No, la situación está controlada.");
        }

        // Finalizar programa
        Console.WriteLine("\nPresione cualquier tecla para salir...");
        Console.ReadKey();
    }
}
