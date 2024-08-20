# gitlab 변경 파일 재구성 후 재가동
gitlab-ctl reconfigure

# gitlab 중지
gitlab-ctl stop

# gitlab 시작
gitlab-ctl start

# gitlab 재시작
gitlab-ctl restart

# gitlab daemon 상태 확인
gitlab-ctl status

# gitlab root 접속 패스워드 파일 위치
/etc/gitlab/initial_root_password

# gitlab 구동 시 확인사항
gitlab.rb 파일에 external_url이 설정되어 있어야 정상 구동됩니다.

# gitlab daemon 구동 실패 시 status
root@127:/# gitlab-ctl status
run: gitaly: (pid 538) 348s; run: log: (pid 572) 345s
run: gitlab-kas: (pid 766) 316s; run: log: (pid 779) 315s
run: logrotate: (pid 500) 360s; run: log: (pid 508) 359s
run: postgresql: (pid 590) 327s; run: log: (pid 601) 326s
run: redis: (pid 516) 354s; run: log: (pid 529) 351s
run: sshd: (pid 40) 380s; run: log: (pid 39) 380s

# gitlab daemon 구동 성공 시 status
root@127:/# gitlab-ctl status
run: alertmanager: (pid 1428) 38s; run: log: (pid 1118) 120s
run: gitaly: (pid 1435) 38s; run: log: (pid 572) 517s
run: gitlab-exporter: (pid 1397) 41s; run: log: (pid 1034) 138s
run: gitlab-kas: (pid 766) 488s; run: log: (pid 779) 487s
run: gitlab-workhorse: (pid 1366) 42s; run: log: (pid 967) 152s
run: logrotate: (pid 500) 532s; run: log: (pid 508) 531s
run: nginx: (pid 1384) 41s; run: log: (pid 1008) 146s
run: postgres-exporter: (pid 1447) 38s; run: log: (pid 1144) 114s
run: postgresql: (pid 590) 499s; run: log: (pid 601) 498s
run: prometheus: (pid 1409) 40s; run: log: (pid 1095) 127s
run: puma: (pid 913) 165s; run: log: (pid 920) 164s
run: redis: (pid 516) 526s; run: log: (pid 529) 523s
run: redis-exporter: (pid 1399) 41s; run: log: (pid 1062) 134s
run: sidekiq: (pid 928) 159s; run: log: (pid 937) 158s
run: sshd: (pid 40) 552s; run: log: (pid 39) 552s

