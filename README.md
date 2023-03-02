# isfibo

class Solution {
  public:
    long long solve(int N, int K, vector<long long> GeekNum) {
        // code here
            long long int sum=0;
            for(int i=0;i<K;i++){
                sum+=GeekNum[i];
               }
            for(int i=K;i<N;i++){
                GeekNum.push_back(sum);
                sum+=GeekNum[i]-GeekNum[i-K];
                
            }
            return GeekNum[GeekNum.size()-1];
    }
};
