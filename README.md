using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Exam_Five
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());
            int m = 1;
            int f = n;

            Console.WriteLine("@{0}@{0}@", new string(' ', n - 2));
            Console.WriteLine("**{0}*{0}**", new string(' ', n - 3));

            for (int i = 1; i <= (n / 2) - 2; i++)
            {
                Console.WriteLine("*{0}*{1}*{2}*{1}*{0}*", new string('.', i), new string(' ', f - 5), new string('.', m));
                f -= 2;
                m += 2;
            }
            Console.WriteLine("*{0}*{1}*{0}*", new string('.', (n / 2) -1), new string('.', n - 3));
            Console.WriteLine("*{0}{1}.{1}{0}*", new string('.', n / 2), new string('*', (n - 1) - (n / 2 + 1)));
            Console.WriteLine("{0}", new string('*', (n * 2) - 1));
            Console.WriteLine("{0}", new string('*', (n * 2) - 1));

        }
    }
}

