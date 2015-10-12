# c_hashmap

This is a simple C hashmap, using strings for the keys.

This is a fork of Zaks Wang's code.

I have translated some of the comments and plan on tidying up the code a bit later on.

I am hoping to use this in a pretty cool project later on.

## credits

This code is based on Zaks Wang's code, which can be found [here](https://github.com/ultimate010/c_hashmap).

They based their code on [Pete Warden's code](https://github.com/petewarden/c_hashmap), which was based on
[Elliot Beck's code](http://elliottback.com/wp/hashmap-implementation-in-c/).

Here's some messages from Zaks Wang:

        1.fix bug that put same key the map value will increase

        2.add feature that you can change hash function

        You can chose SIMPLE_HASH RS_HASH JS_HASH PJW_HASH ELF_HASH BKDR_HASH DJB_HASH AP_HASH
        CRC_HAHS

main.c contains an example that tests the functionality of the hashmap module.

To compile it, run something like this on your system:

gcc main.c hashmap.c hash.c -o hashmaptest

There are no restrictions on how you reuse this code.

Not yet translated:


hash_func_test
##############

        一个字符串hash函数的评测,原文http://blog.csdn.net/liuben/article/details/5050697
        实际语料测试结果，BKDR_HASH远远高于其他HASH函数，其次是AP_HASH
        如果冲突，建议将MAX_CHAIN_LENGTH设置稍大

hashMap
#######

        cheungmine修改版hashmap http://blog.csdn.net/cheungmine/article/details/7704686


待解决的问题：
        仅仅一个数组保存pair的指针，当分配8亿多长度的数组时候，内存会不够，可以分为多段数组，
        再用一个hash解决在多个数组间跳跃问题。有时间再改!
