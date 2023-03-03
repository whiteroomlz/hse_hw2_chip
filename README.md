# hse_hw2_chip
Ссылка на блокнот: https://colab.research.google.com/drive/1elEtbpRMJ_uMEinhMEw76_ihUj5yNlYy?usp=sharing
# Обязательная часть
## FastQC
### ENCFF000AMD - реплика №1
Проверка пройдена, фильтрация и/или подрезание не требуются:

![image1](https://github.com/whiteroomlz/hse_hw2_chip/blob/5df58b14acab42d70cdb059166d8365529179f11/raw/fastQC-report-part-12.png)

### ENCFF000AMB - реплика №2
Не прошли тесты "Per base sequence quality" и "Per tile sequence quality":

![image2](https://github.com/whiteroomlz/hse_hw2_chip/blob/5df58b14acab42d70cdb059166d8365529179f11/raw/fastQC-report-part-11.png)
![image3](https://github.com/whiteroomlz/hse_hw2_chip/blob/5df58b14acab42d70cdb059166d8365529179f11/raw/fastQC-report-part-8.png)
![image4](https://github.com/whiteroomlz/hse_hw2_chip/blob/5df58b14acab42d70cdb059166d8365529179f11/raw/fastQC-report-part-6.png)
![image5](https://github.com/whiteroomlz/hse_hw2_chip/blob/5df58b14acab42d70cdb059166d8365529179f11/raw/fastQC-report-part-4.png)
![image6](https://github.com/whiteroomlz/hse_hw2_chip/blob/5df58b14acab42d70cdb059166d8365529179f11/raw/fastQC-report-part-2.png)

Требуется подрезание. Для этого использовал trimmomatic. В результате значительное улучшение, однако, проблему с расхождением теоретического и наблюдаемого распределений решить не удалось:

![image7](https://github.com/whiteroomlz/hse_hw2_chip/blob/5df58b14acab42d70cdb059166d8365529179f11/raw/fastQC-report-part-9.png)
![image8](https://github.com/whiteroomlz/hse_hw2_chip/blob/5df58b14acab42d70cdb059166d8365529179f11/raw/fastQC-report-part-7.png)
![image9](https://github.com/whiteroomlz/hse_hw2_chip/blob/5df58b14acab42d70cdb059166d8365529179f11/raw/fastQC-report-part-5.png)
![image10](https://github.com/whiteroomlz/hse_hw2_chip/blob/5df58b14acab42d70cdb059166d8365529179f11/raw/fastQC-report-part-3.png)
![image11](https://github.com/whiteroomlz/hse_hw2_chip/blob/5df58b14acab42d70cdb059166d8365529179f11/raw/fastQC-report-part-1.png)

### ENCFF000AHV - контроль
Проверка пройдена, фильтрация и/или подрезание не требуются:

![image12](https://github.com/whiteroomlz/hse_hw2_chip/blob/5df58b14acab42d70cdb059166d8365529179f11/raw/fastQC-report-part-10.png)

## Таблица со статистикой

|ChIP-seq                |ENCFF000AMD       |ENCFF000AMB       |ENCFF000AHV            |
|:-----------------------|:----------------:|:----------------:|:---------------------:|
|TOTAL READS             | 63845894         | 36577885         |     148605824         |
|aligned exactly 1 time  | 4686621 (7.34%)  | 1513483 (4.14%)  | 10662212 (7.17%)      |
|aligned >1 times        | 10415859 (16.31%)| 2880962 (7.88%)  | 23856946 (16.05%)     |
|aligned 0 times         | 48743414 (76.35%)| 32183440 (87.99%)| 114086666 (76.77%)    |

Проанализируйте выдачу bowtie. Почему процент выравниваний получился именно таким?

Выравнивание производилось с прицелом только на одну хромосому из-за ограничения на ресурсы со стороны Google Colab. То есть была взята очень небольшая часть всего генома.

## Диаграммы Эйлера-Венна

![pdf1](https://github.com/whiteroomlz/hse_hw2_chip/blob/dd652bf09e3e044c17b402323faad87dbbee24b1/raw/venn-4-1.png)
![pdf2](https://github.com/whiteroomlz/hse_hw2_chip/blob/dd652bf09e3e044c17b402323faad87dbbee24b1/raw/venn-3-1.png)
![pdf3](https://github.com/whiteroomlz/hse_hw2_chip/blob/dd652bf09e3e044c17b402323faad87dbbee24b1/raw/venn-2-1.png)
![pdf4](https://github.com/whiteroomlz/hse_hw2_chip/blob/dd652bf09e3e044c17b402323faad87dbbee24b1/raw/venn-1-1.png)
