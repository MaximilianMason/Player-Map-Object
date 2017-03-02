# Player-Map-Object
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace StubbedClasses
{
    class Program
    {
        private int gold;
        private int score;
        private int arrows;
        private int turns = 0;
        
        public int[] createHazards()
        {
            int[] r = new int[5];
            return r;
        }
        public int[] turnPassed()
        {
            int[] playerData = new int[4];
            return playerData;
        }
        public int[] moved(int room)
        {
            int[] r = new int[4];
            return r;
        }
        public int encountered(int room)
        {
            return 0;
        }
        public int[] trivia(int triviaAnswered)
        {
            int[] r = new int[4];
            return r;
        }
        public int[] store()
        {
            int[] r = new int[4];
            return r;
        }
    }
}
