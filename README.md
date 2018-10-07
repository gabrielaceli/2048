# #include <iostream>
using namespace std;

int matriz[4][4];
int Fila[] = (1, 0, -1, 0);
int Columna[] = (0, 1, 0, -1);

void NuevoJuego(){
   for(int i = 0; i < 4; i++)
       for(int j = 0; j < 4; j++)
           matriz[i][j] = 0;

}

void printMenu(){
   for(int i = 0; i < 4; i++){

       for(int j = 0; j < 4; j++)
           if (matriz[i][j]==0)
               cout << " ";
           else
               cout << matriz[i][j];
       cout << "\n";
   }
   cout << "n: Nuevo juego, w: subir, s: bajar, d: derecha, a: izquierda, q: quitar\n";
}

int main (){

   while(true){
       printMenu();
       char comandos;
       cin >> comandos;
       if (comandos == 'n')
           NuevoJuego();
       else if(comandos == 'q')
           break;
   }
   return 0;
}
