# mini-blog
Краткое описание проекта
Страницы, которые должны отображаться, их URL-адреса и другие требования, перечислены ниже:

Page	URL	Requirements
Home page	/ and /blog/	Страница индекса, описывающая сайт.
List of all blog posts	/blog/blogs/	
Список всех сообщений блога:

Доступно для всех пользователей из боковой панели.
Список отсортирован по дате публикации (от самого нового до самого старого).
Список разбит на группы по 5 статьям.
Элементы списка отображают название блога, дату публикации и автора.
Названия сообщений блога связаны с страницами подробных сведений о блоге.
Blogger (имена авторов) связаны с страницами подробных сведений о блоге.
Blog author (blogger) detail page	/blog/blogger/<author-id>	
Информация для указанного автора (по id) и список постов:

Доступен для всех пользователей по ссылкам на автора в сообщениях в блогах и т. Д.
Содержит некоторые биографические данные в blogger/author.
Список отсортирован по дате добавления (от новых к старым).
Не разбит на страницы.
Элементы списка отображают только имя сообщения в блоге и дату публикации.
Названия блога связаны со страницей блога.
Blog post detail page	/blog/<blog-id>	
Сведения о блоге.

Доступно для всех пользователей из списков блога.
Страница содержит сообщение в блоге: имя, автор, дата публикации и содержание.
Комментарии к сообщению в блоге должны отображаться внизу.
Комментарии должны быть отсортированы по порядку: от старых до самых последних.
Содержит ссылку для добавления комментариев на конец для зарегистрированных пользователей (см. Страницу формы комментариев)
В блогах и комментариях должен отображаться только обычный текст. Нет необходимости поддерживать какую-либо разметку HTML (например, ссылки, изображения, полужирный / курсив и т. Д.).
List of all bloggers	/blog/bloggers/	
Список блогеров в системе:

Доступный для всех пользователей с боковой панели сайта
Имя блогера связано с блогом автора страницы.
Comment form page	/blog/<blog-id>/create	
Создать комментарий для публикации в блоге:

Доступно только зарегистрированным пользователям (только) из ссылки внизу страницы с подробными сведениями блога.
Отображает форму с описанием для ввода комментариев (дата публикации и блог недоступны для редактирования).
После того, как комментарий будет опубликован, страница будет перенаправлена ​​на связанную страницу блога.
Пользователи не могут редактировать или удалять свои сообщения.
Вышедшие пользователи будут перенаправлены на страницу входа в систему, чтобы добавить комментарии. После входа в систему они будут перенаправлены на страницу блога, которую они хотели бы прокомментировать.
Страницы комментариев должны содержать имя / ссылку на комментарий блога.
User authentication pages	/accounts/<standard urls>	
Стандартные страницы аутентификации Django для входа, выхода и установки пароля:

Вход / выход должен быть доступен через ссылки боковой панели.
Admin site	/admin/<standard urls>	
Админ-сайт должен быть включён, чтобы разрешить создание / редактирование / удаление сообщений в блогах, авторов блога и комментариев блога (это механизм для создания блогеров в блогах):

В админ панеле должен отображаться список комментариев в строке (внизу каждого сообщения в блоге).
Имена комментариев в админке создаются усеканием описания комментария до 75 знаков
Другие типы записей могут использовать базовую регистрацию.
Кроме того, вы должны написать некоторые базовые тесты для проверки:

Все поля модели имеют правильную метку и длину.
Все модели имеют ожидаемое имя объекта (например, __str__() выдаёт ожидаемое значение).
Модели имеют ожидаемый URL для отдельных записей в блогах и комментариях (например, get_absolute_url() возвращает ожидаемый URL-адрес).
Страница BlogListView (страница на всех блогах) доступна в ожидаемом месте (например, /blog/blogs)
Страница BlogListView (страница на всех блогах) доступна на ожидаемом именованном URL-адресе (например, 'blogs')
Страница BlogListView (страница на всех блогах) использует ожидаемый шаблон (например, по умолчанию)
BlogListView разбивает записи на 5 (по крайней мере, на первой странице)
