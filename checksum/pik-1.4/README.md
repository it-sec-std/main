h1. ������ XML-������ ������������ ������������ ���

XML �������� �������� ������� ������������ ������������ ���, �� ���� �������� ����� ������� ����� ������ �����.

h2. �������� xml ������� ������ ������ 1.4

������ ������� ��� �������� ������ xml � �������������� ��������� 
<pre>
<?xml version="1.0" encoding="UTF-8" ?>
</pre>

*PROJECT* - �������� ���
��������:
* version - ������ ������� ������ xml (1.4 ��� ������� ������)
* name - ��� �������
* start_time - ����� ������ �����������
* end_time - ����� ����� �����������

*ALGORITHMS* ���������� ������ *PROJECT*. �������� ���� � ����������� �� �������������� ���������� �����������.
�������� �����������.

*ALGORITHM* ���������� ������ *ALGORITHMS*. �������� ���������� �� �������� ������� ��������� � ����� ���������.
��������:
* short_name - �������� ������������ ���������. [[algorithms|������ �����������]].
* full_name - �������� ���������, ��� ����������� � ������� ��� �����

*FILTERS* ���������� ������ *PROJECT*. �������� ���� � ����������� �� �������������� ������ ������. 
��������:
* case_sensitivity �������� ���������� � ������������������� ��������. ����� ���� *true* ��� *false*.
�������� �����������.

*FILTER* ���������� ������ *FILTERS*. �������� ������ � ������ �����.
��������:
* value �������� �������

*LOCATIONS* ���������� ������ *PROJECT*. �������� ���������� �� ������������� ��������.
�������� �����������.

*LOCATION* ���������� ������ *LOCATIONS*. �������� ������ ���� ������� *ITEM*, �������������� ����� ������������� ������
��������:
* path - ���������� ���� � �������������� �������, ������� ��� �������

*ITEM* ���������� ������ *LOCATION* ��� ������ ������� *ITEM*. �������� ���������� � ����������� �������. ����� ��������� � ���� ���� *ITEM* � *CHECKSUM*. �� ����� ������, ��� item ������� ������������� �� ����, ����� �� �����. ���������� ���������� ���������� �����, ��� ��������� ������� ������������ �� �� �������� ��������� � utf8. 

������ (�������� ����� �������� � �� �������� �����������)
----------------------------------------------------------

<?xml version="1.0" encoding="UTF-8" ?>

<PROJECT version="1.2" name="" start_time="1341230214" end_time="1341230214">
        <ALGORITHMS>
                <ALGORITHM short_name="md5" full_name="MD5"/>
        </ALGORITHMS>
        <FILTERS case_sensitivity="false">
                <FILTER value="*.c" />
        </FILTERS>
        <LOCATIONS>
                <LOCATION path="/media/truecrypt3/pik.repo/bin_stable/bin_stable/iputils-20071127_old">
                        <ITEM type="dir" name="iputils-20071127_old" mtime="1340895883" ctime="1340895883" size="">
                                <ITEM type="file" name="arping.c" mtime="1197273382" ctime="1340201312" size="11477">
                                        <CHECKSUM algorithm="md5" value="fd8211178f97f258b456260764546a83"/>
                                </ITEM>
                                <ITEM type="file" name="clockdiff.c" mtime="1197273382" ctime="1340201312" size="16179" >
                                        <CHECKSUM algorithm="md5" value="6917f57b2d4821b592eb3c4ade01d512"/>
                                </ITEM>
                                <ITEM type="dir" name="Modules" mtime="1280860950" ctime="1340201312" size="">
                                        <ITEM type="file" name="pg3.c" mtime="1197273382" ctime="1340201312" size="15506" >
                                                <CHECKSUM algorithm="md5" value="c8e8044294d639c1af639dd317529ec9"/>
                                        </ITEM>
                                        <CHECKSUM algorithm="md5" value="39efd52d00a202785d8a55ede00b0524"/>
                                </ITEM>
                                <CHECKSUM algorithm="md5" value="6c5531d0c12bdc3b8fc825662b3aedc6"/>
                        </ITEM>
                </LOCATION>
        </LOCATIONS>
        <CHECKSUM algorithm="md5" value="6c5531d0c12bdc3b8fc825662b3aedc6"/>
</PROJECT>