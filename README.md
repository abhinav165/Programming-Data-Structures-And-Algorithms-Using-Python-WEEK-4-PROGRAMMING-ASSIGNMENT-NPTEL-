# my-first-rep
##A python program for calculating the maximum and minimum number of occurrences in a list.(using dictionaries)
def frequency(l):
    x={}
    minlist=[]
    maxlist=[]
    for i in l:
        x[i] = x.get(i,0) + 1
    minvalues=min(x.values())
    for key in x.keys():
        if x[key]==minvalues:
            minlist.append(key)
            
    maxvalues=max(x.values())
    for key in x.keys():
        if x[key]==maxvalues:
            maxlist.append(key)
    minlist.sort()
    maxlist.sort()
    return(minlist,maxlist)
print(frequency([13,12,11,13,14,13,7,11,13,14,12]))
print(frequency([13,12,11,13,14,13,7,11,13,14,12,14,14]))
