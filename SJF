#include <stdio.h>

int main() {
    int at[10], bt[10], temp[10];
    int i, smallest, count = 0, time, n;
    double wait_time = 0, turnaround_time = 0, end;
    float average_waiting_time, average_turnaround_time;

    printf("Enter the number of processes -- ");
    scanf("%d", &n);

    for (i = 0; i < n; i++) {
        printf("Enter Arrival Time and Burst Time for Process P%d -- ", i);
        scanf("%d %d", &at[i], &bt[i]);
        temp[i] = bt[i]; 
    }

    bt[9] = 9999; 

    for (time = 0; count != n; time++) {
        smallest = 9;
        for (i = 0; i < n; i++) {
            if (at[i] <= time && bt[i] < bt[smallest] && bt[i] > 0) {
                smallest = i;
            }
        }
        bt[smallest]--;

        if (bt[smallest] == 0) {
            count++;
            end = time + 1;
            wait_time += end - at[smallest] - temp[smallest];
            turnaround_time += end - at[smallest];
        }
    }

    average_waiting_time = wait_time / n;
    average_turnaround_time = turnaround_time / n;

    printf("\nAverage Waiting Time = %.2f", average_waiting_time);
    printf("\nAverage Turnaround Time = %.2f\n", average_turnaround_time);

    return 0;
}
