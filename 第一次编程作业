import re
import json
text = input()
str_ = {}
str_['number'] = re.findall('\d{11}',text)
str_['name'] = text.split(',',1)[0]
position1 = text.find('1')
position2 = position1 + 11
text = text[3:position1]+text[position2:]
location_str = []
location_str.append(text)
import cpca
df = cpca.transform(location_str,)
df=df.values[0]
str_['number'].extend(df)
str_['number'].insert(0,str_['name'])
final = str_['number']
last1 = final.pop()
last2 = ' '
a = last1.find('街道')
if a != -1 :
    last2 = last1.split('街道')[1]
    last1 = last1.split('街道')[0]
    last1 = last1 + '街道'
a = last1.find('乡')
if a!= -1 :
    last2 = last1.split('乡')[1]
    last1 = last1.split('乡')[0]
    last1 = last1 + '乡'
a = last1.find('镇')
if a != -1 :
    last2 = last1.split('镇')[1]
    last1 = last1.split('镇')[0]
    last1 = last1 + '镇'
final.append(last1)
final.append(last2)
name = final[0]
tel = final[1]
addresslist = final[2:]
dict = {"姓名": name, "手机": tel, "地址": addresslist}
answer=json.dumps(dict,ensure_ascii=False)
print(answer)

