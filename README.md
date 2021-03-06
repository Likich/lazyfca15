# English version
_Russian version below_
We are solving the task of binary classification. It means that there are only 2 possible values for target class. Usually they are denoted by signs + and -. You are given train set, for which you know its class value.
On the other hand, you are given test dataset: there are examples with features, but without class label.
The simple vesion implies that all your features (descriptions of objects) are also binary

You are about to use so-called lazy method. It means that the step of building classificator is eliminated. As soon as you get test object you try to assign class label to it, using existing data from training set.

To solve the problem you are given the framework base on "generators"

# "Generators" method
You split your train data into two parts: C+ - context with "+" examples, C- - context with "-" examples.
To classify object g you have to follow the procedure:
1) for each object from C+ <img src="https://latex.codecogs.com/gif.latex?g_i%5E&plus;"/> you have to calculate intersection with the description of the object to classify (g'); and check, whether this description is presented in any example from C-
2) do the same thing vice versa for C- - for each object description from C- calculate intersection and check whether this intersection is common with any object description from C+

You will have to explore possible step functions for classification.

For instance: you classify object as +, if for intersection with examples from C+ you have no more than x counter-examples; and for descriptions with no counterexamples the size of intersection (cardinality) is at least min_cardinality 


# lazyfca15
Сроки:
01/12 - рабочий код для всего цикла анализа алгоритмов
08/12 - реализация и отчет по собственным доработкам для одного dataset'а
15/12 - реализация поиска оптимальных параметров обучения на нескольких dataset'ах, поиск "глобального" оптимума
22/12 - поддержка нешкалированных данных, финальный отчет


Модификации:
1) собственный набор данных (dataset)
2) пересмотр пространства признаков в имеющихся dataset'ах
3) реализация ленивой распределенной схемы
4) поддержка онлайн схемы поступления данных (учет корректировки реального значения после прогноза)2) пересмотр пространства признаков в имеющихся dataset'ах

Lazy Learning with FCA toolbox hometask

Метрики качества
* True Positive
* True Negative
* False Positive
* False Negative
* True Positive Rate
* True Negative Rate
* Negative Predictive Value
* False Positive Rate
* False Discovery Rate
* Accuracy
* Precision
* Recall
