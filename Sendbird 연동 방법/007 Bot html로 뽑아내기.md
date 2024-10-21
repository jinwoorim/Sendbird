# Bot Chat 화면 html로 뽑아내기

- 아래 코드에서 ApplicationId 와 BotId만 수정해주면됨

```html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Test Bot</title>
    <!-- Load React first and then, ReactDOM. Also, these two libs' version should be same -->
    <script crossorigin src="https://unpkg.com/react@18.2.0/umd/react.development.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@18.2.0/umd/react-dom.development.js"></script>
    <!-- Load chat-ai-widget script and set process.env to prevent it get undefined -->
    <script>
        window.process = { env: { NODE_ENV: 'production' } };
    </script>
    <script crossorigin src="https://unpkg.com/@sendbird/chat-ai-widget@latest/dist/index.umd.js"></script>
    <link href="https://unpkg.com/@sendbird/chat-ai-widget@latest/dist/style.css" rel="stylesheet" />
    <!--Optional; to enable JSX syntax-->
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    <style>
        html,
        body {
            height: 100%
        }

        #aichatbot-widget-close-icon {
            display: none
        }
    </style>
</head>

<body>
    <!-- div element for chat-ai-widget container -->
    <div id="root"></div>
    <!-- Initialize chat-ai-widget and render the widget component -->
    <script type="text/babel">
        const { ChatWindow } = window.ChatAiWidget;
        const App = () => {
            return (
                <ChatWindow applicationId="9357E9F7-7DB5-4CFF-8391-AB9201248D7B" botId="4in-OIKeFI04aj1ytnGiD" />
            );
        };
        ReactDOM.createRoot(document.querySelector('#root')).render(<App />);
    </script>
</body>

</html>



```
