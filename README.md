# imtzb.github.io
pblog
关于find()--function的使用
# Define a procedure, find_last, that takes as input
# two strings, a search string and a target string,
# and returns the last position in the search string
# where the target string appears, or -1 if there
# are no occurrences.
#
# Example: find_last('aaaa', 'a') returns 3
 #   line16:#find()输出一个位置之后，target的第一个位置
#    line17:#输出last_pos+1之后第一个target位置    
 #   line18:#直到从last_pos之后没有target了，输出值为-1，return结束while循环
  #  line20:#将前一个target的位置pos赋值last_pos，继续再一次从last_pos+1开始find()    
# Make sure your procedure has a return statement.

def find_last(search, target):
    last_pos = -1
    while True:                              
        pos = search.find(target, last_pos+1)
        if pos == -1:      
            return last_pos
        last_pos = pos     

print find_last('aaaa', 'a')
#>>> 3

print find_last('aaaaa', 'aa')
#>>> 3

print find_last('aaaa', 'b')
#>>> -1

print find_last("111111111", "1")
#>>> 8

print find_last("222222222", "")
#>>> 9

print find_last("", "3")
#>>> -1

print find_last("", "")
#>>> 0
