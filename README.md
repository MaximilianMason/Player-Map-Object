# Player-Map-Object
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace PlayerMapObject
{
    public class PlayerMapObject
    {
        private int gold;
        private int score;
        private int arrows;
        private int turns;
        private int pit1;
        private int pit2;
        private int bat1;
        private int bat2;
        private int wumpus;
        
        public PlayerMapObject()
        {
            Random num = new Random();
            gold = 5;
            score = 0;
            arrows = 3;
            turns = 0;    
            pit1 = num.next(1, 31);
            pit2 = num.next(1, 31);
            bat1 = num.next(1, 31);
            bat2 = num.next(1, 31);
            wumpus = num.next(1, 31);
        }

        public int[] getHazards()
        {
            int[] hazardLoc = new int[5];
            hazardLoc[0] = pit1;
            hazardLoc[1] = pit2;
            hazardLoc[2] = bat1;
            hazardLoc[3] = bat2;
            hazardLoc[4] = wumpus;
            return hazardLoc;
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
