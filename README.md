# Useful-Codes
常用代码块

## 爬虫相关

### requests（设置session）
```
def webcapture(url):
    headers = {
   # pretend I am a browser
   'User-Agent': 'Mozilla/5.0',
   }
    session = requests.Session() #setup session
    data = session.get(url, headers=headers) #scrape the data
    soup = BeautifulSoup(data.text, 'html.parser') #parse the data
    return soup #return the parsed data
```


### 创建文件夹，把爬虫内容写入文件
```
import os 

folder_name = user_name + ' ' + str(datetime.datetime.now().strftime('%Y-%m-%d %H_%M'))
folder_path = os.getcwd()+ '\\' + folder_name

# create folder with folder_path
if not os.path.exists(folder_path):
    os.makedirs(folder_path)

# set & combine file name
file_name = user_name + ' ' + str(minp).zfill(zfill_n) + '.html'
name_wdir = os.path.join(folder_path, file_name)
        with open(name_wdir, "w", encoding='utf-8') as f:
            f.write(str(soup))
            
```

### 读取文件夹内容
```
import blob
import os
os.listdir() #获取当前文件夹下所有文件名
blob.blob(folder_path + '\\*.html') #读取文件夹内所有html文件
```


    
##  其他
### 正则表达式
```
pattern = re.compile(r'...')
re.finditer(pattern, string) # 返回str内pattern出现的次数
```


### 解决plt中文乱码
```
import matplotlib.pyplot as plt
%matplotlib inline
plt.rcParams['font.sans-serif'] = ['SimHei'] #解决中文乱码
plt.rcParams['axes.unicode_minus'] = False #解决符号问题
```
