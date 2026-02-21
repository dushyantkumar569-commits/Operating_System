#include <stdio.h>

int main() {
    int n, i;
    int bt[20], at[20], wt[20], tat[20], ct[20];
    float wtavg = 0, tatavg = 0;

    printf("Enter the number of processes -- ");
    scanf("%d", &n);

    for (i = 0; i < n; i++) {
        printf("Enter Arrival Time for process P%d -- ", i);
        scanf("%d", &at[i]);
        printf("Enter Burst Time for process P%d -- ", i);
        scanf("%d", &bt[i]);
    }

    ct[0] = at[0] + bt[0];
    for (i = 1; i < n; i++) {
        if (at[i] > ct[i - 1]) {
            ct[i] = at[i] + bt[i];
        } else {
            ct[i] = ct[i - 1] + bt[i];
        }
    }

    for (i = 0; i < n; i++) {
        tat[i] = ct[i] - at[i];
        wt[i] = tat[i] - bt[i];
        wtavg += wt[i];
        tatavg += tat[i];
    }

    printf("\nPROCESS \t ARRIVAL \t BURST \t WAITING \t TURNAROUND\n");
    for (i = 0; i < n; i++) {
        printf("P%d \t\t %d \t\t %d \t %d \t\t %d\n", i, at[i], bt[i], wt[i], tat[i]);
    }

    printf("\nAverage Waiting Time -- %.2f", wtavg / n);
    printf("\nAverage Turnaround Time -- %.2f", tatavg / n);

    return 0;
}
