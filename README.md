def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    else:
        pivot = arr[0]
        left = [x for x in arr[1:] if x < pivot]
        right = [x for x in arr[1:] if x >= pivot]
        return quick_sort(left) + [pivot] + quick_sort(right)

# 範例: 33, 67, 8, 13, 54, 119, 3, 84, 25, 41
example_list = [33, 67, 8, 13, 54, 119, 3, 84, 25, 41]
print("原始數列:", example_list)
sorted_list = quick_sort(example_list)
print("排序後數列:", sorted_list)
