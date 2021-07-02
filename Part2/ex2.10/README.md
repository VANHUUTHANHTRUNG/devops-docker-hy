# Reason #

-   To successfully pass the test, all of the buttons must send request to
    `http://localhost:8080/ping`.
-   With the nginx proxy, all request sent to `http://localhost:80/api/` ( which equals to
    `http://localhost/api` because 80 is the default port ) will be redirected to
    `http://backend:8080/`
-   In `pingpong.js` file reveals that each button calls a pingpong function.
-   The current `REACT_APP_BACKEND_URL` is `http://localhost:8080` in `Dockerfile`
    for front-end app. The result of this setting is : the 3 first buttons with nginx
    will send request to `http://localhost:8080/ping` which is not what we want.
-   The correct URL must start with `http://localhost/api/ping`.
-   The baseURL in `pingpong.js` must be similar to the URL used in pingpongNginx.
-   **Solution**: change value of `REACT_APP_BACKEND_URL` into `http://localhost/api/`
and rebuild then run with `docker-compose up --build`

