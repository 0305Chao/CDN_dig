### ����
��������ְ������д��һ��������linux �ն˿��ٲ�ѯȫ�� CDN ������������ڵ�Ĺ��ߣ������Զ������Ժ�IP��ѯ���ݿ��ѴӴ�����ȥ������
����������������ķ�װ��

dig @119.29.29.29 www.baidu.com  +client=218.203.160.194


### ��Ŀ��ַ
https://github.com/avyou/CDN_dig

### ��Ҫ����

- ֧�ֵ��š���ͨ���ƶ�����ͨ���������������������Ĳ�ѯ��
- ���� dig �� EDNS ���ܣ��ܿ��������ѯ���,������Ҫ��ȫ������ڵ㣻
- ֧����������Ӫ�̻���ʡ�ݱ�����ָ����ѯ��
- ֧��ָ��IP��ѯ���ȣ�֧�ָ���EDNS��
- ֧�ָ���IP��ѯ�ӿ�, ��ѯʧ��ѯ�ӿ�; 
- ֧�����CDN���ȸ��ǵ�ͳ�ƽ����
- ֧�ֶ�IP��ַ��ѯ��whereip����

### �÷�
#### cdig ����
		cdig -d <--domain> [-h <--help>] [-i,--ip>] [-a,--isp] [-n,--edns]

        ������
              -d, --domain=: �����Ҫ�Ĳ�ѯ��������ѡ��.
              -h, --help:    ������Ϣ.
              -i, --ip=:     �����Ҫ��ѯ��IP����ѡ������������ -a��--isp=ѡ�� ��Ĭ�ϲ鿴ȫ������.
                             ��� --ip �� --isp ͬʱָ����ֻȡ--ip.
              -a, --isp=:    �����������ctl-gd����ʾҪ��ѯ�ͻ���IP�ڹ㶫���ŷ���ʱ���������ȵ�����.���ISP�ö��ŷָ�. --isp �ı���ӳ���� %s �ļ�.
              -n, --edns=:   ʹ��ָ������֧��EDNS��IP���н�������ѡ��Ĭ���� 119.29.29.29
        ������
              1). sudo cdig --domain=www.duowan.com --isp=cmb-sd           ##��ѯ������ɽ���ƶ�����������
              2). sudo cdig --domain=www.duowan.com --isp=cmb-sd,cnc-sd    ##��ѯ���ISP�ö��ŷָ�
              3). sudo cdig --domain=www.duowan.com --isp=cmb              ##��ѯ������ȫ���ƶ�����������,��ѯ���ISP�ö��ŷָ�
              4). sudo cdig --domain=www.duowan.com --isp=ctl,cnc          ##��ѯ���ISP�ö��ŷָ� 
              5). sudo cdig --domain=www.duowan.com --ip=1.1.1.1           ##��ѯ��������1.1.1.1����������
              6). sudo cdig --domain=www.duowan.com                        ##��--ip��--ISPѡ�Ĭ��ʹ�ò�ѯȫ������
              7). sudo cdig --domain=www.duowan.com --edns=8.8.8.8         ##ָ������EDNS��:8.8.8.8
              8). sudo cdig --domain=otafs.coloros.com.cloudglb.com. --ip 113.9.222.69   ## �Ӻ�׺ cloudglb.com ���н���ָ������

#### whereip ����
�����ģ�¿��� ��nali�� ���ܵĹ��ߣ�������������Լ�д�Ĵ��룬���������IP��ѯ�ӿڣ����˶Թܵ�������ļ�����Ĳ�ѯ����Ű档

whereip  <ip|ip_file>
cmd |whereip

������

    1. whereip  202.117.112.3
	2. whereip  202.117.112.3  219.146.1.66 
	3. echo "202.117.112.3" |whereip
	4. whereip  ip.txt
	5. cat ip.txt |whereip
	

### ��ͼ

![Alt text](https://github.com/avyou/CDN_dig/blob/master/document/img/cdn_dig_01.png)

![Alt text](https://github.com/avyou/CDN_dig/blob/master/document/img/cdn_dig_02.png)

![Alt text](https://github.com/avyou/CDN_dig/blob/master/document/img/cdn_dig_03.png)

![Alt text](https://github.com/avyou/CDN_dig/blob/master/document/img/whereip_01.png)

![Alt text](https://github.com/avyou/CDN_dig/blob/master/document/img/whereip_02.png)

![Alt text](https://github.com/avyou/CDN_dig/blob/master/document/img/whereip_03.png)

### ��װ˵��



https://github.com/avyou/CDN_dig/document/INSTALL.md
























