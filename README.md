# C_sokoban
C 프로젝트 소코반을 위한 어어어 모임입니다!!

#include <stdio.h>
int c, x=-1, y=0;
int x_Bd, y_Bd;
int Site[40][40];
int main (void)
{
   while ((c=getchar()) != EOF)
  {
      x++;
      Site[y][x] = c;
       if(c == 10)
      {
         y++;
         x_Bd = x;
         x = -1;
      }
   }
    y_Bd = y;
    printf("x_Bd = %d\n",x_Bd);
   printf("y_Bd = %d\n",y_Bd);
   x=-1;
   y=0;
   while(x != x_Bd-1 || y != y_Bd)
   {
      x++;
      printf("Site[%d][%d] = %d\n",y,x,Site[y][x]);
      if(x == x_Bd)
      {
         y++;
         x=-1;
      }
    }
     return 0;
}
