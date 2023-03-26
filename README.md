result = []
def divider(a, b):
    if not isinstance(a, int) or not isinstance(b, int):
        raise TypeError("Both a and b should be integers")
    if b == 0:
        raise ZeroDivisionError("b should not be zero")
    if a < b:
        raise ValueError("a should be greater than or equal to b")
    if b > 50:
        raise IndexError("b should be less than or equal to 50")
    return a/b

data = {10: 2, 2: 5, "123": 4, 18: 0, []: 15, 8 : 4}
for key in data:
    try:
        res = divider(key, data[key])
        result.append(res)
    except Exception as e:
        print(f"An error occurred: {type(e).__name__} - {e}")

print(result)
