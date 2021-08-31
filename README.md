 # ChatBot
<p align="center">       
<img src="https://user-images.githubusercontent.com/41328887/131534044-c90e5780-18c5-43c7-82a6-4b7b8f05696e.png" width="324" height="324">
</p>

# Implementación
Deberás instalar las dependencias correspondiente

- MessagePack 2.2.113 (Nugget)
- AIRH_IA (Agregar desde referencia)

Cargar el método 
StartBot();
al inicio del programa y luego usar el método string 
RespuestaBot(string input) esto devolverá la respuesta del 
bot a lo que le allá escrito.

# Entrenamiento
Para poder "entrenar" el bot, adjunto un programa con el cual
podrás realizar dicha acción de manera fácil rápida y sencilla,
una vez agregado las parabras y las respectivas respuestas,
deberás copiar la carpeta creada y pegarla en la ruta raíz del 
proyecto dónde tienes la dll y eso sería todo.

#Ejemplo (Console App)

        static void Main(string[] args)
        {
            Wellcome();

            while (Salir)
            {
                Console.ForegroundColor = ConsoleColor.Blue;
                string Pregunta = Console.ReadLine().Trim();

                if (Pregunta.Equals("salir"))
                {
                    Salir = false;
                }
                else
                {
                    Console.ForegroundColor = ConsoleColor.DarkRed;
                    Console.WriteLine(AIRH_IA.Bot.RespuestaBot(Pregunta));
                    Console.WriteLine("");
                }
            }
            Console.WriteLine("");
            Console.ForegroundColor = ConsoleColor.Yellow;
            Console.WriteLine("Aplicación Finalizada");
            Console.ReadKey();
        }
        
         private static void Wellcome()
        {
            Console.ForegroundColor = ConsoleColor.Green;
            AIRH_IA.Bot.StartBot();
            Console.WriteLine("==============================");
            Console.WriteLine("¡Bienvenido/a al ChatBot AIRH!");
            Console.WriteLine("==============================");
            Console.ForegroundColor = ConsoleColor.Yellow;
            Console.WriteLine("");
            Console.WriteLine(@"- Escriba ""Salir"" para cerrar el programa.");
            Console.WriteLine("");
        }
