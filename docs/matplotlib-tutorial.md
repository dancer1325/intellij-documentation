[//]: # (Source: https://www.jetbrains.com/help/idea/matplotlib-tutorial.html)
[//]: # (Downloaded: 2025-12-17 19:32:05)

## Add sample code

Create an empty [Python project](creating-empty-python-project.html). Add a new Python file named  main.py  by right-clicking the project root and selecting New | Python File. Then add the following code to the  main.py  file:

import numpy as np import matplotlib.pyplot as plt N = 50 x = np.random.rand(N) y = np.random.rand(N) colors = np.random.rand(N) area = np.pi * (15 * np.random.rand(N))**2 # 0 to 15 point radii plt.scatter(x, y, s=area, c=colors, alpha=0.5) plt.show() X = np.linspace(-np.pi, np.pi, 256,endpoint=True) C,S = np.cos(X), np.sin(X) plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-") plt.plot(X, S, color="red", linewidth=2.5, linestyle="-") plt.xlim(X.min()*1.1, X.max()*1.1) plt.xticks([-np.pi, -np.pi/2, 0, np.pi/2, np.pi], [r'$-\pi$', r'$-\pi/2$', r'$0$', r'$+\pi/2$', r'$+\pi$']) plt.ylim(C.min()*1.1,C.max()*1.1) plt.yticks([-1, 0, +1], [r'$-1$', r'$0$', r'$+1$']) plt.show() 

Process warnings shown for the `numpy` and `matplotlib` imports and enable the packages in the project.
