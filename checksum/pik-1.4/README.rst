h1. Формат XML-отчета контрольного суммирования ПИК

XML является основным отчетом контрольного суммирования ПИК, на базе которого можно создать любой другой отчет.

h2. Описание xml формата отчёта версии 1.4

Первой строкой идёт указание версии xml и использованной кодировки 
<pre>
<?xml version="1.0" encoding="UTF-8" ?>
</pre>

*PROJECT* - корневой тег
Атрибуты:
* version - версия формата отчёта xml (1.4 для текущей версии)
* name - имя проекта
* start_time - время начала хеширования
* end_time - время конца хеширования

*ALGORITHMS* содержится внутри *PROJECT*. Содержит теги с информацией по использованных алгоритмам хеширования.
Атрибуты отсутствуют.

*ALGORITHM* содержится внутри *ALGORITHMS*. Содержит информацию по отдельно взятому алгоритму в своих атрибутах.
Атрибуты:
* short_name - короткая аббревиатура алгоритма. [[algorithms|Список аббревиатур]].
* full_name - название алгоритма, для отображения в отчетах для людей

*FILTERS* содержится внутри *PROJECT*. Содержит теги с информацией по использованных маскам файлов. 
Атрибуты:
* case_sensitivity Содержит информацию и регистрозависимости фильтров. Может быть *true* или *false*.
Атрибуты отсутствуют.

*FILTER* содержится внутри *FILTERS*. Содержит строку с маской файла.
Атрибуты:
* value Значение фильтра

*LOCATIONS* содержится внутри *PROJECT*. Содержит информацию об анализируемых локациях.
Атрибуты отсутствуют.

*LOCATION* содержится внутри *LOCATIONS*. Содержит только один элемент *ITEM*, представляющий собой анализируемый объект
Атрибуты:
* path - абсолютный путь к местоположению объекта, включая имя объекта

*ITEM* содержится внутри *LOCATION* или внутри другого *ITEM*. Содержит информацию о суммируемом объекте. Может содержать в себе теги *ITEM* и *CHECKSUM*. На одном уровне, все item сначала отсортированы по типу, затем по имени. Сортировка аналогична сортировке строк, где отдельные символы сравниваются по их числовым значениям в utf8. 

Пример (значения хешей случайны и не являются корректными)
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
