from ast import literal_eval
height_list = [('zhangsan',173),('lisi',179),('wangwu',160),('liuliu',167),('hanqi',171),('wuba',176),('xiejiu',180),('fengshi',177)]
copy_list = height_list.copy()
tup = ()
# （1easy） 计算队列目前的成员个数；
print(len(height_list))
# （2medium）计算该队列中成员的平均身高；
i = 1
for i in range(len(copy_list)):
    copy_list[i] = copy_list[i][1:]
    tup = copy_list[i] + tup
print(sum(tup)/len(tup))
#[literal_eval(",".join(i)) for i in copy_list]
#print(copy_list)
# （3medium）返回该队列中身高为180的成员姓名及所在位置；
ls = list(tup)
ls.reverse()
if 180 in ls:
    print(ls.index(180)+1)
else:
    print('Not find!')
# （4easy）该队列现加入一人，姓名：liming，身高：164，现将其添加至该队列最后端，请返回更新后的身高列表height_list；
height_list.append(('liming',164))
print(height_list)
# （5easy）该队列现加入一人，姓名：weilin，身高：175，现将其添加至该队列最前端，请返回更新后的身高列表height_list；
height_list.reverse()
height_list.append(('weilin',175))
height_list.reverse()
print(height_list)
# （6hard选做不计分）根据身高从小到大的顺序对以上表进行排序，返回最终的排序结果。


