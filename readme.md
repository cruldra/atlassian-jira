# 准备工作
如果jira被nginx代替并使用https协议,需要先修改``server.xml``文件中的``proxyName``、``proxyPort``、``scheme``三个参数,如下:
```xml
<Connector   proxyName="todo.cruldra.com" proxyPort="443" scheme="https"  />
```
# 启动
```bash
git clone https://github.com/cruldra/atlassian-jira.git jira
```