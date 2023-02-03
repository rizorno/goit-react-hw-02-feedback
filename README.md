# goit-react-hw-02-feedback

# Критерії приймання

Використовуй цей
[шаблон React-проекту](https://github.com/goitacademy/react-homework-template#readme)
як стартову точку своєї програми.

- Створений репозиторій `goit-react-hw-02-feedback`.
- При здачі домашньої роботи є посилання на репозиторій з вихідним кодом
  проекту. У шапці репозиторія є посилання на живу сторінку на `GitHub pages`.
- Під час відвідування робочої сторінки (GitHub pages) завдання, в консолі
  відсутні помилки і попередження.
- Для кожного компонента є окремий файл у папці `src/components`.
- Для всіх компонентів описані `propTypes`.
- Все, що компонент очікує у вигляді пропсів, передається йому під час виклику.
- Імена компонентів зрозумілі та описові.
- JS-код чистий та зрозумілий, використовується `Prettier`.
- Стилізація виконана `CSS-модулями` або `Styled Components`.

## Завдання 1 - Віджет відгуків

Як і більшість компаній, кафе Expresso збирає відгуки від своїх клієнтів. Твоє
завдання – створити додаток для збору статистики. Є лише три варіанти зворотного
зв'язку: добре, нейтрально і погано.

### Крок 1

Застосунок повинен відображати кількість зібраних відгуків для кожної категорії.
Застосунок не повинен зберігати статистику відгуків між різними сесіями
(оновлення сторінки).

Стан застосунку обов'язково повинен бути наступного вигляду, додавати нові
властивості не можна.

```js
state = {
  good: 0,
  neutral: 0,
  bad: 0,
};
```

Інтерфейс може мати такий вигляд.

https://textbook.edu.goit.global/lms-react-homework/v1/uk/img/hw-02/feedback/step-1.png

### Крок 2

Розшир функціонал застосунку таким чином, щоб в інтерфейсі відображалося більше
статистики про зібрані відгуки. Додай відображення загальної кількості зібраних
відгуків з усіх категорій та відсоток позитивних відгуків. Для цього створи
допоміжні методи `countTotalFeedback()` і `countPositiveFeedbackPercentage()`,
які підраховують ці значення, ґрунтуючись на даних у стані (обчислювані дані).

https://textbook.edu.goit.global/lms-react-homework/v1/uk/img/hw-02/feedback/step-2.png

### Крок 3

Виконай рефакторинг застосунку. Стан застосунку повинен залишатися у кореневому
компоненті `<App>`.

Винеси відображення статистики в окремий компонент
`<Statistics good={} neutral={} bad={} total={} positivePercentage={}>`. Винеси
блок кнопок в компонент `<FeedbackOptions options={} onLeaveFeedback={}>`.
Створи компонент `<Section title="">`, який рендерить секцію із заголовком і
дітей (children). Обгорни кожен із `<Statistics>` і `<FeedbackOptions>` у
створений компонент секції.

### Крок 4

Розшир функціонал застосунку таким чином, щоб блок статистики рендерився тільки
після того, як було зібрано хоча б один відгук. Повідомлення про відсутність
статистики винеси в компонент `<Notification message="There is no feedback">`.

https://textbook.edu.goit.global/lms-react-homework/v1/uk/img/hw-02/feedback/preview.gif
