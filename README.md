# lecture_40_JS_Events  
#  [Задачи ](https://github.com/schoolteacherMP/lecture_40_JS_Events/blob/main/tasks.md)    

Есть три способа назначения обработчиков событий:  
**Атрибут HTML**: onclick="...".  
**DOM-свойство**: elem.onclick = function.  
**Специальные методы**: elem.addEventListener(event, handler[, phase]) для добавления, removeEventListener для удаления.  

HTML-атрибуты используются редко потому, что JavaScript в HTML-теге выглядит немного странно. К тому же много кода там не напишешь.  

DOM-свойства вполне можно использовать, но мы не можем назначить больше одного обработчика на один тип события. Во многих случаях с этим ограничением можно мириться.  

Последний способ самый гибкий, однако нужно писать больше всего кода. Есть несколько типов событий, которые работают только через него, к примеру transitionend и DOMContentLoaded. Также addEventListener поддерживает объекты в качестве обработчиков событий. В этом случае вызывается метод объекта handleEvent.  

Не важно, как вы назначаете обработчик – он получает объект события первым аргументом. Этот объект содержит подробности о том, что произошло.  

**События мыши:**  

**click** – происходит, когда кликнули на элемент левой кнопкой мыши (на устройствах с сенсорными экранами оно происходит при касании).  
**contextmenu** – происходит, когда кликнули на элемент правой кнопкой мыши.  
**mouseover** / **mouseout** – когда мышь наводится на / покидает элемент.  
**mousedown** / **mouseup** – когда нажали / отжали кнопку мыши на элементе.  
**mousemove** – при движении мыши.  

**События на элементах управления:**  
**submit** – пользователь отправил форму `<form>`.  
**focus** – пользователь фокусируется на элементе, например нажимает на `<input>`.  
**Клавиатурные события:**  
**keydown** и **keyup** – когда пользователь нажимает / отпускает клавишу.  
  
**События документа:**  
**DOMContentLoaded** – когда HTML загружен и обработан, DOM документа полностью построен и доступен.  
  
**CSS events:**  
**transitionend** – когда CSS-анимация завершена.  

