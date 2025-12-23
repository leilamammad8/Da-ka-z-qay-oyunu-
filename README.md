#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int user, comp;

    printf("Das-Kagiz-Qayci Oyunu\n");
    printf("1 - Das\n");
    printf("2 - Kagiz\n");
    printf("3 - Qayci\n");
    printf("Seciminizi daxil edin: ");
    scanf("%d", &user);

    srand(time(NULL));
    comp = rand() % 3 + 1;

    printf("Kompüterin secimi: %d\n", comp);

    if (user == comp) {
        printf("Beraberlik!\n");
    }
    else if (
        (user == 1 && comp == 3) ||
        (user == 2 && comp == 1) ||
        (user == 3 && comp == 2)
    ) {
        printf("Siz qalib geldiniz!\n");
    }
    else {
        printf("Kompüter qalib geldi!\n");
    }

    return 0;
}
