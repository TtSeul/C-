using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _2._2._2
{
    class Program
    {
        static void Main(string[] args)
        {
            double eleve = 0, jour = 0, nourriture = 0, hebergement = 0, hebergementTotal = 0, total = 0;
            string chaineSaisie;
            
            //Saisie
            Console.WriteLine("Saisir le nombre d'élève : ");
            chaineSaisie = Console.ReadLine();
            eleve = Convert.ToSingle(chaineSaisie);

            Console.WriteLine("Saisir le nombre de jours : ");
            chaineSaisie = Console.ReadLine();
            jour = Convert.ToSingle(chaineSaisie);

            //Calcul
            if (eleve < 30)
            {
                hebergement = 4.75;
            }
            else if (eleve > 30)
            {
                hebergement = 4;
            }
            else if (eleve > 35)
            {
                hebergement = 3.50;
            }
            nourriture = (3.5 * jour) + (3.5 * eleve);
            hebergementTotal = (hebergement * jour) + (hebergement * eleve);
            total = nourriture + hebergementTotal;

            //Affichage
            Console.WriteLine("Le coût du voyage scolaire sera de : " + total);
            Console.ReadKey();

        }
    }
}
