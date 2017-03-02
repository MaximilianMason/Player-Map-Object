# Player-Map-Object
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace PlayerMapObject
{
    class Program
    {
        private int gold = 5;
        private int score = 0;
        private int arrows = 3;
        private int turns = 0;

        public int[] createHazards()
        {
            int[] r = new int[5];
            return r;
        }
        public int[] turnPassed(Boolean arrowShot)
        {
            int[] playerData = new int[4];
            playerData[0] = gold++;
            if (arrowShot)
                playerData[1] = arrows--;
            else
                playerData[1] = arrows;
            playerData[2] = turns++;
            playerData[3] = score;

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
