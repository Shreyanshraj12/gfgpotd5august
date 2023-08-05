class Solution{
    public:
   long long findMinDiff(vector<long long> a, long long n, long long m){
    //cod
    long long min_diff = INT_MAX;
    sort(a.begin(), a.end());
    for(int i = 0; i + m <= a.size(); i++){
        min_diff = min(min_diff, (a[i+m-1]-a[i]));
    }
    return min_diff;    
    }  
};
