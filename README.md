# Experiment-3

#include <stdio.h>

int main() {
    int arr[100], size = 0;
    int choice, i, pos, element;

    while (1) {
        printf("\n1. Traverse\n2. Insert\n3. Select\n4. Display\n5. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        if (choice == 1) {
            for (i = 0; i < size; i++) {
                printf("Element %d: %d\n", i, arr[i]);
            }
        } else if (choice == 2) {
            printf("Enter position (0 to %d): ", size);
            scanf("%d", &pos);
            printf("Enter element: ");
            scanf("%d", &element);
            for (i = size; i > pos; i--) {
                arr[i] = arr[i - 1];
            }
            arr[pos] = element;
            size++;
        } else if (choice == 3) {
            printf("Enter index: ");
            scanf("%d", &pos);
            if (pos >= 0 && pos < size)
                printf("Element at index %d is %d\n", pos, arr[pos]);
            else
                printf("Invalid index\n");
        } else if (choice == 4) {
            for (i = 0; i < size; i++) {
                printf("%d ", arr[i]);
            }
            printf("\n");
        } else if (choice == 5) {
            break;
        } else {
            printf("Invalid choice\n");
        }
    }

    return 0;
}
