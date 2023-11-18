# week11_js_questions

1. Что такое DOM?

- DOM - это такая разветвлённая модель(форма) повторяющая структуру HTML которая предоставляет доступ языкам прогромирования к содержимому HTML, что позволяет изменять части HTML кода их ститли и т.д Управлять ими.

2. Что такое BOM?

- BOM - это перечень глобальных объектов для управления браузером с помощью програмирования, он как и DOM находится внутри widow.

3. Каким методом можно получить элемент по его идентификатору в DOM?

let Element = document.getElementById("сюда вносится id элемента");
let Element = querySelector('#id элемента');
let Element = querySelectorAll('#id элемента');

4. Каким методом можно создать новый элемент в DOM?

const newElement = document.createElement('input');//создаём элемент в DOM

const bodyElement = dcument.querySelector('body');//выбираем элемент куда вставляем, или относительно которого вставляем

bodyElement.prepend(newElement);//добавит элемент на страницу в начало тег body

5. Каким методом можно добавить класс к элементу в DOM?

- Свойство classList метод add или toggel(если такого class нет то добавит, если есть удалит.)

const newElement = querySelector('div');

newElement.add('new');// добавит class="new"

6. Каким методом можно изменить текстовое содержимое элемента в DOM?

- метод textContent

const newElement = document.querySelector('.new');

newElement.textContent = 'Новый текст';

7. Что такое объект события и какие у него могут быть свойства?

- event - это объект события, который задаётся в качестве параметра, он содержит информацию о событие, которое запускает функцию с параметром event(evt). Поскольку even содержит все события, то свойств у него куча. Но как это работает пока не поняла))

8. Есть элемент: <input id= "input" value = "Привет">. Какой вызов поменяет значение в нём?

const hello = getElementById('input);

hello.value = "Пока";

9. Для чего используется запись: setAttribute(name, value)?

- используется для задания значения атрибуту

10. Как сделать переход на другую страницу при клике на кнопку (без <a href=...>, только средствами JavaScript)?

<body>
  <button id="button" onclick="changePage()">Change Page</button>
	<script>
	    function changePage() {
	      let nextPage = document.getElementById('button');
	      nextPage.location.href ='http//:.......';
	    }
	 </script>
</body>

11. Найдите ошибку в коде, которая мешает изменить цвет текста при нажатии на кнопку.
<body>
  <h1 id="myElement">Hello, World!</h1>
  <button onclick="changeColor()">Change Color</button>
	<script>
	    function changeColor() {
	      let element = document.getElementByid('myElement');//не тот регист у i, нужно getElementById
	      element.style.color = 'red';
	    }
	 </script>
</body>

12. Найдите ошибку в коде, которая мешает добавить новый элемент списка при нажатии на кнопку.

<body>
  <ul id="myList">
    <li>Item 1</li>
    <li>Item 2</li>
  </ul>
  <button onclick="addListItem()">Add Item</button>
  <script>
    function addListItem() {
      let list = document.getElementById('myList');
      let item = document.createElement('li');
      item.textContent = 'New Item';// поменяла innerHTVL on textContent
      list.appendChild(item);// поменяла item on list, добавила Child
    }
  </script>
</body>

13. Найдите ошибку в коде, которая мешает удалить параграф при нажатии на кнопку.

<body>
  <p class="myParagraph">This is a paragraph.</p>
  <button onclick="removeParagraph()">Remove Paragraph</button>//добавила скобки после removeParagraph. Всё равно не работает, не могу понять почему
  <script>
    function removeParagraph() {
      let paragraph = document.getElementsByClassName('myParagraph');
      paragraph.remove();
    }
  </script>
</body>
</html>

14. Найдите ошибку в коде, которая мешает добавить изображение при нажатии на кнопку.

<body>
  <button onclick="showImage()">Показать изображение</button>
</body>
<script>
    function showImage() {
      const img = document.createElement('img');
      img.src = image.jpg;
      document.body.append(img);
    }
</script>
