## nginx 명령 모음

### nginx 기동
<pre>nginx</pre>

### nginx 정지
<pre>nginx -s stop</pre>

### nginx 재기동
<pre>nginx -s reload</pre>

### nginx config 파일 유효성검증
<pre>nginx -t</pre>


## nginx conf 명세
최대 connection 수를 지정합니다. connection 수를 초과할 경우 아래의 응답을 반환합니다.
> 1024 worker_connections are not enough while connecting to upstream
<pre>
events {
    worker_connections  1024;
}
</pre>