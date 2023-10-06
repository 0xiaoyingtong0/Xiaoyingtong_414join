（1）我的昵称叫少司命，这是国漫秦时明月中的一个角色，这个角色的个人魅力很吸引我，就用了她的名字做我的昵称，由此可见我是个爱看动漫的学生。
（2）我叫肖瀛彤，来自北京。我是个活泼开朗、同情心强、责任心强的人。平时喜欢运动，像跑步、跳绳、打羽毛球我都十分擅长。
（3）加入414最想学习的是3D建模，很喜欢二次元的人物，希望自己有朝一日也能创造出自己喜欢的二次元人物。目前建模0基础，后续会进行自学，希望能进414和有经验的学长学姐学习，多和学长学姐交流，开阔眼界的同时提升自己的个人能力。
2.1冒泡算法
冒泡排序：我的理解是从尾部开始比较相邻的两个元素，如果尾部的元素比前一个的元素大，就交换两个元素的位置。往前对每个相邻的元素都做这样的比较、交换，到数组头部时，第 1 个元素会成为最大的元素相当于“冒泡”，然后重新从尾部开始比较大小，除去在这之前头部已经排好的元素。继续对越来越少的数据进行比较、交换操作，直到没有可比较的数据为止，排序就完成了。
冒泡冒的这个泡就是每一趟中从数组里筛出来的最大的数。对于同样大的数是不需要交换位置的，所以数的相对位置不会发生变化。
例如把10,20,30,40,50进行排序，从尾部第一个数开始，比较倒数第一个数和倒数第二个数的大小，如果大，就交换，小就不交换，继续比较倒数第二个数和倒数第三个数的大小，规则同样，直到最后会有一个数“冒泡”也就是50，然后40,30,20,10的顺序会在交换中按大小排列或者除10以外都“冒泡”了，这组数的顺序就排好了。
以下是我找的代码。
public class BubbleSort {
    private int[] array;
   
    public BubbleSort(int[] array) {
        this.array = array;
    }
    /**
     * 从小到大
     */
    public void sort() {
        int length = array.length;
        if (length > 0) {
            for (int i = 1; i < length; i++) {
                for (int j = 0; j < length - i; j++) {
                    if (array[j] > array[j + 1]) {
                        int temp = array[j];
                        array[j] = array[j + 1];
                        array[j + 1] = temp;
                    }
                }
            }
        }
    }
   
    /**
     * 从大到小
     */
    public void sort2() {
        int length = array.length;
        if (length > 0) {
            for (int i = length - 1; i > 0; i--) {
                for (int j = length - 1; j > length - 1 - i ; j--) {
                    if (array[j] > array[j - 1]) {
                        int temp = array[j];
                        array[j] = array[j - 1];
                        array[j - 1] = temp;
                    }
                }
            }
        }
    }
   
    public void print() {
        for (int i = 0; i < array.length; i++) {
            System.out.println(array[i]);
        }
    }
}

}
