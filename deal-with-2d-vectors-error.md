Dealing with 2d-vectors' error
================================================================

# Issue Description
When using 2d-vectors like this

```cpp
#include <vector>
using namespace std;

vector<vector<int>> v;

int main() {
    for (int i = 0; i < 5; i++)
        for (int j = 0; j < 5; j++)
            v[i].push_back(j);

    return 0;
}

```

it is very likely that you will get an error saying

> Segmentation fault (core dumped)

It is because when you try to push back `j` into the 2d vector, you are actually trying to push back it into a vector that does not exist. 

# Solutions

## 01. Define the size

If you are sure about how many vectors you are goint to use at maximum, you can simply aviod this error by defining the 2d-vector this way

```cpp

vector<vector<int>> v(5);

```

But this solution might have several problems, like you might not know how many vectors there will be, or difficult to handle memory.

## 02. Push-back subvectors and

You can first push back empty subvectors, and then push back `j` to them.

In this way, you can avoid pushing back values to non-existing vectors.

```cpp

vector<vector<int>> v;

int main() {
    for (int i = 0; i < 5; i++) {
        vector<int> subvector;
        v.push_back(subvector);
        for (int j = 0; j < 5; j++) {
            v[i].push_back(j);
        }
    }

    return 0;
}

```

So these are simple solutions you can use when you run into a `segmentation fault (core dumped)` error while using 2d-vectors.