# java-agent-demo

# ���빤��
+ cd java-agent-demo
+ mvn package

# ��̬���ش���ʽ(require jdk 6+)
## ����Ӧ�ó���
+ cd java-agent-test
+ ����  java-dynamic-agent-test.bat 
	
	===========JavaAgentTestApp=============
	HelloBean.hello() -> sleep 5 seconds
	HelloBean.hello() -> sleep 5 seconds
	HelloBean.hello() -> sleep 5 seconds

##jps��ѯ����id

	3300 Jps
	7032 java-agent-test-0.1-jar-with-dependencies.jar
	7196

##���д���ͻ���
+ cd java-agent
+ ����  java-agent-client.bat 7032


##�鿴Ӧ�ó�����־�Ѿ����ش�����Ч

	=========Java Agent with Agentmain========
	HelloBean.hello() -> sleep 5 seconds
	HelloBean.hello() -> sleep 5 seconds
	The Method Used Time Is:5001ms.
	HelloBean.hello() -> sleep 5 seconds
	The Method Used Time Is:5000ms.

# �������ش���ʽ(require jdk 5+)
## ����Ӧ�ó���
+ cd java-agent-test 
+ ����java-agent-server.bat

	=========Java Agent with Premain========
	===========JavaAgentTestApp=============
	HelloBean.hello() -> sleep 5 seconds
	The Method Used Time Is:5002ms
	HelloBean.hello() -> sleep 5 seconds
	The Method Used Time Is:6164ms