#include <stdio.h>

int main() {
    printf("B Manohar-192211557\n");
    int size;
    printf("Enter the number of elements: ");
    scanf("%d", &size);

    int array[size];
    printf("Enter the elements: ");
    for (int i = 0; i < size; i++) {
        scanf("%d", &array[i]);
    }

    printf("Original array: ");
    for (int i = 0; i < size; i++) {
        printf("%d ", array[i]);
    }
    printf("\n");

    for (int width = 1; width < size; width *= 2) {
        for (int left = 0; left < size; left += 2 * width) {
            int mid = left + width;
            int right = left + 2 * width;

            if (mid > size)
                mid = size;
            if (right > size)
                right = size;

            int n1 = mid - left;
            int n2 = right - mid;

            int leftArr[n1], rightArr[n2];

            for (int i = 0; i < n1; i++)
                leftArr[i] = array[left + i];
            for (int j = 0; j < n2; j++)
                rightArr[j] = array[mid + j];

            int i = 0, j = 0, k = left;
            while (i < n1 && j < n2) {
                if (leftArr[i] <= rightArr[j]) {
                    array[k] = leftArr[i];
                    i++;
                } else {
                    array[k] = rightArr[j];
                    j++;
                }
                k++;
            }

            // Copy remaining elements, if any
            while (i < n1) {
                array[k] = leftArr[i];
                i++;
                k++;
            }
            while (j < n2) {
                array[k] = rightArr[j];
                j++;
                k++;
            }
        }
    }

    printf("Sorted array: ");
    for (int i = 0; i < size; i++) {
        printf("%d ", array[i]);
    }
    printf("\n");

    return 0;
}
