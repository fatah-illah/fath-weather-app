# API Proxy Server (Node.js)

This is a server used for hiding API keys, rate limiting, and caching. It utilizes the [OpenWeather API](https://openweathermap.org/api) as an example, but it can be easily modified to work with any public API that you may be using.

## Utilization

### Install dependencies

```bash
npm install
```

### Run on http://localhost:5000

```bash
npm run dev
```

### Add information about public API

Rename **.env.example** to **.env** and edit the values

If the public API URL is **https://api.openweathermap.org/data/2.5/weather?q={city}&appid={APIkey}**

- API_BASE_URL = "https://api.openweathermap.org/data/2.5/weather"
- API_KEY_NAME = "appid"
- API_KEY_VALUE = "This is YOUR API KEY"

You can append any additional query parameters as necessary when accessing the /api endpoint, such as https://yourdomain/api?q=detroit, without having to include your API key on the client.

- Add new routes as per your requirement.
- Modify rate limiting and caching to desired values.
