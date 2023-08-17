def flatten(lst):
    flat_list = []
    for item in lst:
        if isinstance(item, list): 
            flat_list.extend(flatten(item)) 
        else:
            flat_list.append(item) 
    return flat_list

# Test
lst = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
print(flatten(lst))

def reverse_nested(lst):
    reversed_list = []
    for item in lst:
        if isinstance(item, list): 
            reversed_list.append(reverse_nested(item)) 
        else:
            reversed_list.append(item)  
    return reversed_list[::-1] 

# Test
lst = [[1, 2], [3, 4], [5, 6, 7]]
print(reverse_nested(lst)) 
