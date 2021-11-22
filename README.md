# java-3-
java实验三 计202 宋明扬 2020310606
# 一、实验目的
1.掌握权限访问控制修饰符的使用
<br>2.掌握继承的使用
# 二、业务要求
1.保持实验二的代码和readme版本不变
<br>2.新建代码仓库，在实验二代码的基础上完成本次实验
<br>3.业务过程同实验二，但在类的设计上，采用父类-子类的继承关系定义
<br>4.测试实体类分别存放于不同的package中，验证权限访问控制、继承后属性及方法的可见性
# 三、实验要求
1.提交源程序到gitee或github，代码仓库命名为“实验三继承关系”
<br>2.写实验报告文件（readme.md），体现本次实验在实验二基础上的改进
# 四、解题思路
## **步骤一**：
&emsp;&emsp;**在实验二的基础上，添加父类Father函数，添加Student和Teacher中的共同的id，name和sex，使Student和Teacher继承父类中的。**
## **步骤二**：
&emsp;&emsp;**对Student类进行改进。
<br>&emsp;&emsp;首先实现选课过程中，重复输入课程号和输入错误课程号时报错。
<br>&emsp;&emsp;在实现清空学生课表的功能，清除所选的全部课程。**
# 五、关键代码
1. 改进了Studengt类里面，xuanke函数，实现了重复输入课程号和输入错误课程号时报错。
```java 
    public void xuanke(int course_id, Course[] stu_c) {
        //输入的课程号与课组里某门课的课号相等，则将该门课添加到学生的个人课程数组里
            int q = 0;
            for (int a = 0; a < stu_c.length; a++) {
                if (stu_c[a] == null) {
                    break;
                }
                else if (course_id == stu_c[a].getId()) {
                    for (int b=0; b<stu_cour.length; b++){
                        if(stu_cour[0] == null) {
                            stu_cour[i] = stu_c[a];
                            i++;
                            System.out.println("您已成功选上该课程！");
                            break;
                        }
                        else if(stu_cour[0] != null){
                            if(course_id == stu_cour[b].getId()){
                                System.out.println("重复选择，请重新操作！");
                                break;
                            }
                            else if (stu_cour[b] == null){
                                break;
                            }

                            else{
                                stu_cour[i] = stu_c[a];
                                i++;
                                System.out.println("您已成功选上该课程！");
                                break;
                            }
                        }
                    }
                    q = 1;
                    break;
                }

            }
            if(q == 0){
                System.out.println("课程号输入错误，请重新操作！");
            }
        }
```
2. 定义父类Father。
```
package xuankeSystem;

public class Father {
    private String name;
    private int id;
    private String sex;

    public Father(int id, String name, String sex){
        setId(id);
        setName(name);
        setSex(sex);
    }

    public String getName(){
        return name;
    }
    public void setName(String name){
        this.name = name;
    }

    public int getId(){
        return id;
    }
    public void setId(int id){
        this.id = id;
    }

    public String getSex(){
        return sex;
    }
    public void setSex(String sex){
        this.sex = sex;
    }

}
```
# 六、系统运行截图
&emsp;&emsp;下图是本实验主程序TestBanking.java的运行结果。
<br>![avatar](https://github.com/songmingyang01/java-3-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202021-11-22%20111109.png)
<br>![avatar](https://github.com/songmingyang01/java-3-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202021-11-22%20110752.png)
<br>![avatar](https://github.com/songmingyang01/java-3-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202021-11-22%20110813.png)
<br>![avatar](https://github.com/songmingyang01/java-3-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202021-11-22%20110823.png)
# 七、感想与体会
&emsp;&emsp;
