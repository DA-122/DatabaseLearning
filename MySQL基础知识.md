## SQL��������


## SELECT���ִ�й���
һ��SELECT�������ܽ�Ϊ���¾�ʽ��

`SELECT XXX FROM XXX WHERE XXX GROUP BY XXX HAVING XXX ORDER BY XXX LIMIT XXX;`

* 1.FROM ��䣬��������ݱ��ļ����ص��ڴ�ȥ��
* 2.WHERE ��䣬���1���е����ݽ��й��ˣ�ȡ�����������ļ�¼������һ����ʱ��(1)��
* 3.SELECT ��䣬 
  * ���û��GROUP BY����ֱ�Ӹ����ֶζ���ʱ������SELECT���õ���ʱ��(2)��
  * �����GROUP BY���Ὣ��ʱ��1�зֳɶ����ʱ���ֱ�ִ��SELECT����ֻȡ���еĵ�һ����¼��Ȼ�����γ��µ���ʱ��(2)��
* 4.HAVING ��䣬ֻ������GROUP BY֮��HAVING�Ƕ�SELECT֮�����ʱ���е����ݽ��й��ˣ����SELECT����û�е��ֶβ�������HAVING֮��
* 5.ORDER BY ��䣬��������ʱ��(2)�����ֶν�������
* 6.LIMIT ��䣬ȡ������ǰ���ٸ�Ԫ�ء�