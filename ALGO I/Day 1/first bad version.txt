public class Solution extends VersionControl {
    public int firstBadVersion(int n) {
        
       long  i=1;
        long j=n;
        long mid;
        int fbv=n;
        while(i<=j){
            mid=(i+j)/2;
            if(isBadVersion((int)mid)){
                j=(int)mid-1;
                fbv=(int)mid;
            }else{
                i=(int)mid+1;
            }
        }
        return fbv;
        
    }
}