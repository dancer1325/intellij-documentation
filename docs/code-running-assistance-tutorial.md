[//]: # (Source: https://www.jetbrains.com/help/idea/code-running-assistance-tutorial.html)
[//]: # (Downloaded: 2025-12-17 19:20:17)

## Prerequisites

  * You have already created a Python project and populated it with the following code: 

import math def demo(a, b, c): d = b ** 2 - 4 * a * c if d > 0: disc = math.sqrt(d) root1 = (-b + disc) / (2 * a) root2 = (-b - disc) / (2 * a) return root1, root2 elif d == 0: return -b / (2 * a) else: return "This equation has no roots" if __name__ == '__main__': a = int(input("a: ")) b = int(input("b: ")) c = int(input("c: ")) result = demo(a, b, c) print(result) 

  * You have Python interpreter already [configured](configuring-python-sdk.html). Note that for the current project your Python interpreter version should be 3.0 or later.



