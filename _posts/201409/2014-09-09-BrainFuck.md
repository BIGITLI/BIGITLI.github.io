---
layout: post
title: BrainFuck编译器
description: BrainFuck编译器的java实现
categories:
- Hadoop 
tags:
- vagrant
---


###BrainFuck编译器的java实现

#####Brainfuck简介
+ Brainfuck是一种极小化的计算机语言，它是由Urban Müller在1993年创建的。由于fuck在英语中是脏话，这种语言有时被称为brainf*ck或brainf***，甚至被简称为BF。

+ 这种语言基于一个简单的机器模型，除了指令，这个机器还包括：一个以字节为单位、被初始化为零的数组、一个指向该数组的指针(初始时指向数组的第一个字节)、以及用于输入输出的两个字节流。

   下面是这八种状态的描述，其中每个状态由一个字符标识：
    
　　字符 含义
   
　　＞ 指针加一
  
　　＜ 指针减一
  
　　\+ 指针指向的字节的值加一
　　
　　\- 指针指向的字节的值减一
　　
　　. 输出指针指向的单元内容(ASCII码)
  
　　, 输入内容到指针指向的单元(ASCII码)
  
　　[ 如果指针指向的单元值为零，向前跳转到对应的]指令的次一指令处
  
　　] 如果指针指向的单元值不为零，向后跳转到对应的[指令的次一指令处
  
　　(按照更节省时间的简单说法，"]"也可以说成“向后跳转到对应的"["状态”。这两解释是一样的。)
  
　　(第三种同价的说法，"["意思是"向前跳转到对应的"]""，]意思是"向后跳转到对应的[指令的次一指令处，如果指针指向的字节非零。")


       /**
         * BrainFuck 编译器
         *
         * @author: chenzhigang
         * @version:
         * date: 2014年8月25日
         * mailto: chenzhigang@foxmail.com
         * blog : http://chenzhigang.github.io/
         * review 
         */
        public class BrainFuckMachine {
            static int[] datas = new int[2048]; //状态区域
            static int p	= 0 ; //状态区域的指针
            static int pc 	=0; //命令的指针
            public static void main(String[] args) {
                //String code ="++++++++++[>++++++++++<-]>++++.+.";
                String code="++++++++++[>+++++++>++++++++++>+++>+<<<<-]"
                        + ">++.>+.+++++++..+++.>++."
                        + "<<+++++++++++++++.>.+++.------.--------.>+.>.";
                run(code);
            }
            public static void run(String code){
                char[] cmds = code.toCharArray();
                while(true){
                    switch(cmds[pc]){
                    case '>':
                        p++;
                        break;
                    case '<':
                        p--;
                        break;
                    case '+':
                        datas[p]++;
                        break;
                    case '-':
                        datas[p]--;
                        break;
                    case '.':
                        System.out.print((char)datas[p]);
                        break;
                    case ',':
                        break;
                    case '[':
                        if(datas[p] ==0){
                            findNext(cmds);
                        }
                        break;
                    case ']':
                        if(datas[p] !=0){
                            findPre(cmds);
                        }
                        break;
                    }
                    pc++;
                    if(pc > cmds.length-1){
                        System.out.println();
                        System.out.println("程序运行结束 !");
                        break;
                    }
                }
            }
            /**
             * 向后找 ]
             * @param cmds
             */
            public static void findNext(char[] cmds){
                while(true){
                    pc++;
                    if(pc > cmds.length-1){
                        System.out.println("代码不符合语法规范");
                        return;
                    }
                    if(cmds[pc]==']'){
                        return;
                    }

                }
            }

            /**
             * 向前找 [ 
             * @param cmds
             */
            public static void findPre(char[] cmds){
                while(true){
                    pc--;
                    if(pc < 0){
                        System.out.println("代码不符合语法规范");
                        return;
                    }
                    if(cmds[pc]=='['){
                        return;
                    }
                }
            }
        }

