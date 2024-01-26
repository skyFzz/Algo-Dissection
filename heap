def maxPush(arr, item):
    arr.append(float("-inf"))
    maxIncrease(arr, len(arr) - 1, item)

def maxIncrease(arr, i, item):
    arr[i] = item
    parentI = i // 2 if i % 2 != 0 else i // 2 - 1
    while i > 0 and arr[parentI] < arr[i]:
        arr[i], arr[parentI] = arr[parentI], arr[i]
        i = parentI
        parentI = i // 2 if i % 2 != 0 else i // 2 - 1

def maxPop(arr):
    item, arr[0] = arr[0], arr[len(arr) - 1]
    newArr = arr[:len(arr) - 1]
    maxHeapify(newArr, 0)
    
    return item

def buildMaxHeap(arr):
    for i in range(len(arr) // 2 - 1, 0, -1):
        maxHeapify(arr, i)

def maxHeapify(arr, i):
    left = 2 * i + 1
    right = 2 * i + 2
    l = len(arr)
    largest = 0

    if left < l and arr[left] > arr[i]:
        largest = left
    else:
        largest = i
    if right < l and arr[right] > arr[largest]:
        largest = right
    if largest != i:
        arr[i], arr[largest] = arr[largest], arr[i]
        maxHeapify(arr, largest)
