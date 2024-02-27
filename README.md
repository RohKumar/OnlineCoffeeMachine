Designed and implemented an HTTP API that controls an internet-connected coffee machine. This solution fulfils the following criteria:
1. When the endpoint GET /brew-coffee is called, the endpoint returns a 200 OK status code with a status message and the current date/time in the response body as a JSON object, with the date/time formatted as an ISO-8601 value e.g. { “message”: “Your piping hot coffee is ready”, “prepared”: “2021-02-03T11:56:24+0900” };
2. On every fifth call to the endpoint defined in #1, the endpoint returns 503 Service Unavailable with an empty response body, to signify that the coffee machine is out of coffee;
3. If the date is April 1st, then all calls to the endpoint defined in #1 returns 418 I’m a teapot instead, with an empty response body, to signify that the endpoint is not brewing coffee today (see https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/418);

Non-functional Feature:
1. Implemented in .NET Core
2. Included Unit tests for several scenarios.

Additional Feature:
1. When the endpoint GET /brew-coffee is called, the endpoint check a third-party weather service (e.g. https://openweathermap.org/api), and if the current temperature is greater than 30°C, the returned message be changed to “Your refreshing iced coffee is ready”;
2. Original feature #2 and #3 remains same.
