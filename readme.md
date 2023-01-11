# 准备工作
如果jira被nginx代替并使用https协议,需要先修改``server.xml``文件中的``proxyName``、``proxyPort``、``scheme``三个参数,如下:
```xml
<Connector   proxyName="todo.cruldra.com" proxyPort="443" scheme="https"  />
```
# 启动
```bash
git clone https://github.com/cruldra/atlassian-jira.git jira && \
cd jira && \
docker-compose up -d
```

# 迁移
迁移就是把``jira``和``mysql``两个目录打包传到新的服务器上去
```bash
cd jira && \
tar -zcvf jira.tar.gz jira && \
tar -zcvf mysql.tar.gz mysql
```
然后在你的新服务器上解压
```bash
cd jira && \
tar -zxvf jira.tar.gz && \
tar -zxvf mysql.tar.gz
```