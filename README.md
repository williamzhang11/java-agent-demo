# java-agent-demo

# ���빤��
+ cd java-agent-demo
+ mvn package

# ��̬���ش���ʽ(require jdk 6+)
1.����java-dynamic-agent-test.bat���൱������Ӧ�ó���

	HelloBean.hello() -> sleep 5 seconds
	HelloBean.hello() -> sleep 5 seconds
	HelloBean.hello() -> sleep 5 seconds

2.jps��ѯ����id

	3300 Jps
	7032 java-agent-test-0.1-jar-with-dependencies.jar
	7196

3.����java-agent-client.bat 7032


4.�鿴���г����Ѿ����ش�����Ч

	HelloBean.hello() -> sleep 5 seconds
	HelloBean.hello() -> sleep 5 seconds
	The Method Used Time Is:5001ms.
	HelloBean.hello() -> sleep 5 seconds
	The Method Used Time Is:5000ms.

# �������ش���ʽ(require jdk 5+)
����java-agent-server.bat