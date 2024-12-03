[![CI/CD GitHub Actions](https://github.com/Elrimio/Test2.0/actions/workflows/python-app.yml/badge.svg)](https://github.com/Elrimio/Test2.0/actions/workflows/python-app.yml)
[![Coverage Status](https://coveralls.io/repos/github/Elrimio/Test2.0/badge.svg?branch=main)](https://coveralls.io/github/Elrimio/Test2.0?branch=main)
[![Quality Gate](https://sonarcloud.io/api/project_badges/measure?project=Elrimio_Test2.02&metric=alert_status)](https://sonarcloud.io/dashboard?id=Elrimio/Test2.0)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=Elrimio_Test2.0&metric=bugs)](https://sonarcloud.io/summary/new_code?id=Elrimio_Test2.0)
[![Code smells](https://sonarcloud.io/api/project_badges/measure?project=Elrimio_Test2.0&metric=code_smells)](https://sonarcloud.io/dashboard?id=Elrimio_Test2.0)

# План тестирования:

# Аттестационное тестирование
<ol>
   <li>
      <h4> Тест А1 (положительный) </h4>
      <ul>
         <li> Начальное состояние: Открытый терминал </li>
         <li> Действие: Пользователь запускает программу</li>
         <li> Ожидаемый результат: Выводится список с доступными операциями</li>
      </ul>
   </li> 
   <li>               
      <h4> Тест А2 (положительный) </h4>
      <ul>
         <li> Начальное состояние: Выбор операции </li>
         <li> Действие: Пользователь вводит 1(Сложение матриц) </li>
         <li> Ожидаемый результат: Выводится поле для ввода параметров матрицы </li>
      </ul>
   </li>           
   <li>            
      <h4> Тест А3 (негативный) </h4>
      <ul>
         <li> Начальное состояние: Ввод параметров матрицы </li>
         <li> Действие: Пользователь вводит qwe </li>
         <li> Ожидаемый результат: Сообщение "Ошибка ввода: Введите натуральное число" </li>
      </ul>
   </li>
   <li>            
      <h4> Тест А4 (негативный) </h4>
      <ul>
         <li> Начальное состояние: Ввод элементов матрицы </li>
         <li> Действие: Пользователь вводит qwe </li>
         <li> Ожидаемый результат: Сообщение "Ошибка ввода" </li>
      </ul>
   </li>
   <li>             
      <h4> Тест А5 (положительный) </h4>
      <ul>
         <li> Начальное состояние: Введены параметры двух матриц </li>
         <li> Действие: Пользователь вводит элементы первой и второй матрицы(1,2,3,4)(2,3,4,5)</li>
         <li> Ожидаемый результат: </li>
		 <ul>
			<li>Результат сложения матриц: </li>
			<li>[3.0, 5.0] </li>
			<li>[7.0, 9.0] </li>
		 </ul>
      </ul>
   </li>
   <li>              
      <h4> Тест А6 (положительный) </h4>
      <ul>
         <li> Начальное состояние: Меню выбора операции </li>
         <li> Действие: Пользователь вводит 0 </li>
         <li> Ожидаемый результат: Программа завершена </li>
      </ul>
   </li>
</ol>

# Блочное тестирование
<ol>
  <li>
    <h3>class TestMatrixOperation(unittest.TestCase)</h3>
    <ol>
		<li>
    	  <h4>Тест Б1.1 (положительный) Cложение элементов матриц</h4>
    	  <ul>
    	    <li>Входные данные:</li>
			<ul>
				<li>matrix1 размера 2x2 с элементами [[1, 2], [3, 4]]</li>
			</ul>
    	    <li>Ожидаемый результат: Сумма элементов = 10</li>
    	  </ul>
    	</li>
    	<li>
    	  <h4>Тест Б1.2 (положительный) Cложение матриц</h4>
    	  <ul>
    	    <li>Входные данные:</li>
			<ul>
				<li>matrix1 размера 2x2 с элементами [[1, 2], [3, 4]]</li>
				<li>matrix2 размера 2x2 с элементами [[5, 6], [7, 8]]</li>
			</ul>
    	    <li>Ожидаемый результат: Матрица размера 2x2 с элементами [[6, 8], [10, 12]].</li>
    	  </ul>
    	</li>
    	<li>
    	  <h4>Тест Б1.3 (положительный) Умножение матриц</h4>
    	  <ul>
    	    <li>Входные данные:</li>
			<ul>
				<li>matrix1 размера 2x2 с элементами [[1, 2], [3, 4]]</li>
				<li>matrix2 размера 2x2 с элементами [[5, 6], [7, 8]]</li>
			</ul>
    	    <li>Ожидаемый результат: Матрица размера 2x2 с элементами [[19, 22], [43, 50]].</li>
    	  </ul>
    	</li>
		<li>
    	  <h4>Тест Б1.4 (положительный) Умножения матрицы на скалярную величину</h4>
    	  <ul>
    	    <li>Входные данные:</li>
			<ul>
				<li>matrix1 размера 2x2 с элементами [[1, 2], [3, 4]]</li>
				<li>scalar равный 2</li>
			</ul>
    	    <li>Ожидаемый результат: Матрица размера 2x2 с элементами [[2, 4], [6, 8]].</li>
    	  </ul>
    	</li>
		<li>
    	  <h4>Тест Б1.5 (положительный) Транспонирование матрицы</h4>
    	  <ul>
    	    <li>Входные данные:</li>
			<ul>
				<li>matrix размера 2x3 с элементами [[1, 2, 3], [4, 5, 6]]</li>
			</ul>
    	    <li>Ожидаемый результат: Матрица размера 3x2 с элементами [[1, 4], [2, 5], [3, 6]].</li>
    	  </ul>
    	</li>
		<li>
    	  <h4>Тест Б1.6 (положительный) Вычисление определителя матрицы</h4>
    	  <ul>
    	    <li>Входные данные:</li>
			<ul>
				<li>matrix размера 2x2 с элементами [[1, 2], [3, 4]]</li>
			</ul>
    	    <li>Ожидаемый результат: Определитель матрицы matrix равен -2.</li>
    	  </ul>
    	</li>
		<li>
    	  <h4>Тест Б1.7 (положительный) Вычисление обратной матрицы</h4>
    	  <ul>
    	    <li>Входные данные:</li>
			<ul>
				<li>matrix размера 2x2 с элементами [[4, 7], [2, 6]]</li>
			</ul>
    	    <li>Ожидаемый результат: Матрица размера 2x2 с элементами [[0.6, -0.7], [-0.2, 0.4]].</li>
    	  </ul>
    	</li>
		<li>
    	  <h4>Тест Б1.8 (положительный) Возведение матрицы в степень</h4>
    	  <ul>
    	    <li>Входные данные:</li>
			<ul>
				<li>matrix размера 2x2 с элементами [[2, 1], [1, 2]], степень = 3</li>
			</ul>
    	    <li>Ожидаемый результат: Матрица размера 2x2 с элементами [[14, 13], [13, 14]].</li>
    	  </ul>
    	</li>
		<li>
    	  <h4>Тест Б1.9 (Негативный) Возведение матрицы в степень</h4>
    	  <ul>
    	    <li>Входные данные:</li>
			<ul>
				<li>matrix размера 2x3 с элементами [[2, 1, 3], [1, 2, 0]], степень = 2</li>
			</ul>
    	    <li>Ожидаемый результат: Сообщение об ошибке.</li>
    	  </ul>
    	</li>
		<li>
    	  <h4>Тест Б1.10 (Негативный) Возведение матрицы в степень</h4>
    	  <ul>
    	    <li>Входные данные:</li>
			<ul>
				<li>matrix размера 2x2 с элементами [[1, 0], [0, 1]], степень = 5</li>
			</ul>
    	    <li>Ожидаемый результат: Матрица размера 2x2 с элементами [[1, 0], [0, 1]].</li>
    	  </ul>
    	</li>
    </ol>
  </li>
</ol>

# Интеграционное тестирование
<ol>
  <li>
    <h3>Тест И1</h3>
    <ul>
      <li>Методы: transpose(matrix), determinant(matrix)</li>
      <li>Описание: Проверяем корректность последовательного применения методов транспонирования и вычисления определителя.</li>
      <li>Входные данные: matrix размера 3x3 с элементами [[1, 2, 3], [4, 5, 6], [7, 8, 9]]</li>
      <li>Ожидаемый результат: Определитель транспонированной матрицы должен быть равен 0.</li>
    </ul>	
  </li>
  <li>
    <h3>Тест И2</h3>
    <ul>
      <li>Методы: multiply_matrices(matrix1, matrix2), scalar_multiply(matrix, scalar)</li>
      <li>Описание: Проверяем корректность последовательного применения методов умножения матриц и умножения на скалярную величину</li>
      <li>Входные данные:</li>
	  <ul>
			<li>matrix1 размера 2x2 с элементами [[1, 2], [3, 4]]</li>
			<li>matrix2 размера 2x2 с элементами [[5, 6], [7, 8]]</li>
			<li>scalar равный 2</li>
	  </ul>
      <li>Ожидаемый результат: Матрица размера 2x2 с элементами [[38, 44], [86, 100]].</li>
    </ul>	
  </li>
</ol>
