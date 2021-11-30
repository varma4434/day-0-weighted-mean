#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <iomanip>
#include <algorithm>
using namespace std;


int main() {
    int length;
    vector<int> values;
    vector<int> weights;
    cin >> length;
    for(int i = 0; i < length; i++) {
        string input;
        cin >> input;
        values.push_back(stoi(input));
    }
    for(int i = 0; i < length; i++) {
        string input;
        cin >> input;
        weights.push_back(stoi(input));
    }
    float w_mean;
    float top = 0;
    float bottom = 0;
    for(int i = 0; i < length; i++) {
        top += (values[i] * weights[i]);
        bottom += weights[i];
    }
    cout << setprecision(1) << fixed << top/bottom;
    return 0;
}
