# leanring-algorithm
2、最大子数组和
<br/>
<br/>
class PetApplicationTests {

    @Test
    void contextLoads() {
    }



    @Test
    public static int Demo(int[] nums) {
        int res=nums[0];
        int sum=0;
        for(int num : nums){
            if(sum > 0){
                sum += num;
            }
            else{
                sum = num;
            }
            res = Math.max(res, sum);
        }
        return res;
    }

    public static void main(String[] args){
        int[] nums= {-2,1,-3,4,-1,2,1,-5,4};
        System.out.println("初始值：");
        System.out.println(Arrays.toString(nums));
        Demo(nums);
        System.out.println("输出值：");
        System.out.println(Demo(nums));
    }

}

