# python6
def getMinDiff(arr, n, k):
    arr.sort()

    ans = arr[n - 1] - arr[0]

    for i in range(1, n):
        minEle = min(arr[0] + k, arr[i] - k)
        maxEle = max(arr[i - 1] + k, arr[n - 1] - k)
        ans = min(ans, maxEle - minEle)

    return ans

# Example usage:
arr1 = [1, 5, 8, 10]
n1 = 4
k1 = 2
print(getMinDiff(arr1, n1, k1))  # Output: 5

arr2 = [3, 9, 12, 16, 20]
n2 = 5
k2 = 3
print(getMinDiff(arr2, n2, k2))  # Output: 11
