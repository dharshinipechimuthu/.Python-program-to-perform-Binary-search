# .Python-program-to-perform-Binary-search
def binarySearch(alist, key):
    first = 0
    last = len(alist) - 1
    found = False

    while first <= last and not found:
        midpoint = (first + last) // 2

        if key == alist[midpoint]:
            found = True
        elif key < alist[midpoint]:
            last = midpoint - 1
        else:
            first = midpoint + 1

    if found:
        print(key, "is found in the list", alist, "at position", midpoint + 1)
    else:
        print(key, "is not found in the list")


testlist = [0, 1, 2, 8, 13, 17, 19, 32, 42]
binarySearch(testlist, 13)

testlist = [0, 1, 2, 8, 13, 17, 19, 32, 42]
binarySearch(testlist, 100)

OUTPUT:

13 is found in the list [0, 1, 2, 8, 13, 17, 19, 32, 42] at position 5
100 is not found in the list
