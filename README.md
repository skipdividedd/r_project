## Анализ конструкции "(не) осилить Х"

### Значения конструкции

ФЭБ: "Словарь русского языка (МАС)"
http://feb-web.ru/feb/mas/mas-abc/15/ma264527.htm?cmd=0&istext=1

1. Одержать верх в борьбе, схватке, битве; побороть, одолеть || перен. Пересилить, преодолеть, побороть (какое-л. чувство, волнение и т. п.). 

2. Справиться с чем-л. требующим физических усилий, большой затраты труда и т. п. || Разг. Усвоить, постичь что-л., справиться с чем-л., преодолев какие-л. трудности, затруднения. || Разг. Съесть или выпить что-л. в большом количестве. 

Моя разметка:

1.1. победить, одержать верх в борьбе, схватке, битве (прямое значение);

1.2. перен. пересилить, преодолеть, побороть (метафорическое значение);

2.1. справиться с чем-либо требующим физических усилий, большой затраты труда и т. п.;

2.2. справиться с чем-либо требующим больших денежных трат (т.е. купить / оплатить);

3. усвоить, понять, постичь что-либо (когнитивная сфера);

4. съесть или выпить что-либо в большом количестве.

Таким образом, значения с пометкой "перен.", "разг." получили отдельные пункты; значение 2.2. было также вынесено в отдельный пункт, хотя оно не упоминается в словаре.

### Данные

**Источник: НКРЯ**

Поиск (-не, осилить | осиливать) и (не, осилить | осиливать)

Время: настоящее, прошедшее, будущее

Не вошли: инфинитив, деепричастие, причастие

Всего: 909

Конструкция: 695

**Источник: Twitter**

твиты: since = '2023-04-13' until= '2023-04-20' 

поиск: “осилил”, “осилила”, “осилило”, осилили” (прошедшее время) при помощи twint (Python)

поиск: “ниасилил”, “ниасилила”, “ниасилило”, ниасилили” (прошедшее время) + “осилю”, “осилим”, “осилишь”, осилите”, “осилит”, “осилят” (будущее время) при помощи twint-zero (Go)

Всего: 464

Конструкция: 336

**Разметка НКРЯ**: polarity, semi_neg, Meaning (семантическое значение), tense (время глагола), aspect (вид глагола),  center (глагол 'осилить' в той форме, в которой употребляется в предложении),	normalized (нач. форма глагола), Created (дата создания), X (субъект), Y (объект),	Y_POS (POS объекта),	Y_animacy (одушевленность объекта),	Y_case (падеж объекта),	Full context (предложение), Title (автор + произведение),	Sphere (стиль),	Medium (книга / журнал / газета / etc)

Корпус НКРЯ по грамматике размечался при помощи Python (pymorphy), затем разметка проверялась вручную.

**Разметка Twitter**: polarity, semi_neg, Meaning (семантическое значение), tense (время глагола), center (глагол 'осилить' в той форме, в которой употребляется в предложении), Y (объект), username, date, tweet

Оба корпуса вручную размечались по значениям, по объекту, полярности. 

#### Ограничения

* **1 разметчик**

* **Трудные случаи разметки** 
1) Глагол “осилить” не всегда образует конструкцию, либо ее не всегда можно четко вычленить + может присутствовать эллипсис + встречаются непонятные предложения
Примеры:
а) "Вот смотрела их в инете,чёт мне кажется,не осилю,сложно больно"; "Хорошо, я осилю…" – не размечалось как конструкция;
б) "ссср не сделал ни одного аппарат мрт или узи, а на западе они уже были. в середине 80-х начали завозить, свой так и не осилили" – “не осилили свой” (эллипсис) – конструкция;
в) "NYR не осилят... Очень интересно посмотреть на Бостон не в регулярке и Эдмонтон" – непонятное предложение. 

2) В коротких предложениях не всегда можно разметить по семантике – недостаток контекста. 
Примеры:
"Мой мамонт такое точно осилит"; "Не, ты такое не осилишь"; "А что, стейблкоины отменили?! Или дремучие орки этого не осилят?"

* **Источники**

НКРЯ: книги и публицистика, по большей части.

Twitter: сфера бытового интернет-общения.

### Гипотеза

Употребление конструкции меняется с течением времени. 

а) в целом, конструкция тяготеет к будущему / прошедшему времени, сов. вид (осилить, а не осиливать) и чаще принимает объектом неодушевленный предмет, субъект – одушевленный;

б) конструкция стала чаще употребляться под отрицанием;

в) меняется семантика конструкции –  некоторые значения уходят из дискурса.

Истоки наивной гипотезы: интуитивные наблюдения 

Истоки доработанной гипотезы: чтение данных НКРЯ во время разметки.

### Research design

##### а) описательная статистика, exploratory data analysis;

**Общая формальная гипотеза**

H0: конструкция не тяготеет к определенным значениям присущих ей грамматических категорий.

H1: конструкция чаще употребляется в определенном грамматическом контексте.

##### б) описательная статистика, exploratory data analysis, тест Манна-Уитни, логистическая регрессия, chi-squared test;

**Общая формальная гипотеза**

H0: распределение использования конструкции в негативном и положительном контексте по годам одинаково.

H1: распределения отличаются.

##### в) описательная статистика, exploratory data analysis, prop.test.

**Общая формальная гипотеза**

H0: конструкция равно принимает все семантические значения независимо от корпуса.

H1: в зависимости от корпуса наблюдается сдвиг в сторону определенных семантических значений.
