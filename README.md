# Trianglusing System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Triangle
{
    class Program
    {


        static void Main(String[] args)

        {
            string val = string.Empty;
            int tri = 0;
            string S1;
            string S2;
            string S3;
            Console.WriteLine("options");
            do
            {
                int a = 0;
                int b = 0;
                int c = 0;
                bool d = false;
               
                Console.WriteLine("1.Enter the sides");
                Console.WriteLine("2.Exit");
                string triside = Console.ReadLine();
                int.TryParse(triside, out tri);
                if (tri == 1)
                {
                    do
                    {
                        Console.WriteLine("Enter the first side");
                        S1 = Console.ReadLine();

                        int.TryParse(S1, out a);

                        d = true;


                        Console.WriteLine("Enter the 2nd side");
                        S2 = Console.ReadLine();

                        int.TryParse(S2, out b);

                       

                        Console.WriteLine("Enter the 3rd side");
                        S3 = Console.ReadLine();


                        int.TryParse(S3, out c);
                        
                        val = TriangleSolver.Analyze(a, b, c);

                    } while (d == false);


                    Console.WriteLine("{0}", val);
                }
                else
                {
                    System.Environment.Exit(0);
                }

            } while (tri == 1 || tri == 2);

        


        }

    }




}





