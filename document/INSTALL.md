### ��װ

#### dig���ߵİ�װ
�ű�Ŀǰ������ dig ���ߵ�EDNS����֧�֣��������¿��ܻ��������ʹ��python ��pydig�⡣
```
wget ftp://ftp.isc.org/isc/bind9/9.9.3/bind-9.9.3.tar.gz
tar xf bind-9.9.3.tar.gz
cd bind-9.9.3

wget http://wilmer.gaa.st/edns-client-subnet/bind-9.9.3-dig-edns-client-subnet-iana.diff
patch -p0 < bind-9.9.3-dig-edns-client-subnet-iana.diff
./configure --prefix=/usr/local/dig   --without-openssl
make
```

### ��װ CDN_dig
```
git clone git@github.com:avyou/CDN_dig.git
cd CDN_dig
python setup.py install  
//�����ǰ����һЩ�����ⰲװ���ɹ���������ʹ��pipֱ�Ӱ�װ������Ȼ��������ִ��һ�飬���£�
pip install -r  requirements.txt
```
### ����
���ú������ļ�Ĭ�ϰ�װ��: /usr/local/CDN_dig/�����dig ��װ��·��һ�£�Ĭ�������ǲ����޸ĵģ���װ�꼴��ʹ�á�

####Ŀ¼�ṹ

```
tree
.
������ bin
��   ������ cdig        ##ִ���ļ� ,PATH ·��ͬ����һ��
��   ������ whereip    ##ִ���ļ� ,PATH ·��ͬ����һ��
������ data
��   ������ ip_dns_isp.list   ## ȫ��DNS ip �б��ļ������Լ������
��   ������ ipipdb.dat    ## IP ��ѯ���ݿ⣬github��û��
��   ������ qqwry.dat     ## ����IP ��ѯ���ݿ�
������ etc
    ������ config.ini    ##�����ļ� 

	
```
��Ȼ���а�װ�� python��Ŀ¼����Ҫ�ű��ļ������ﲻд�ˡ�

####�����ļ�����

```
cat /usr/local/CDN_dig/etc/config.ini 
[BASE]
default_api = ip138   ##Ĭ�Ͻӿ�
default_dns = 119.29.29.29    ##Ĭ��EDNS
ipdns_db = /usr/local/CDN_dig/data/ip_dns_isp.list  ##ȫ��DNS��IP�б�
tmp_dir = /tmp/dig    ##���������ļ�����ʱĿ¼
dig = /usr/local/dig/bin/dig   ## dig �������ļ�·��

[API]
ip138 = http://www.ip138.com/ips138.asp?ip=   ##ip138 ץȡ�Ľӿڣ���Ҫץ��̫����^~^
#ipdb = /usr/local/CDN_dig/data/ipipdb.dat    ##ipip���շ�IP��ѯ���ݿ⣬û�ϴ�
chinaz = http://ip.chinaz.com/     ##chinaz ץȡ�Ľӿ�
qqwry = /usr/local/CDN_dig/data/qqwry.dat  ##����IP��ѯ���ݿ�,2018��1�·ݵ�
```








