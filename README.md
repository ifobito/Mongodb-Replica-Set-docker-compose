# Triển khai MongoDB Replica Set cục bộ với docker-compose

Thiết lập cục bộ máy chủ MongoDB với bộ replica bằng cách sử dụng docker-compose

Trình kết nối cơ sở dữ liệu MongoDB sử dụng giao dịch để hỗ trợ các thao tác ghi lồng nhau. Chúng ta sẽ gặp lỗi nếu cố gắng ghi dữ liệu vào cơ sở dữ liệu không hỗ trợ replication.

### Bạn có hai giải pháp:

1. Sử dụng [MongoDB Atlas](https://www.mongodb.com/atlas/database). Đây là một dịch vụ miễn phí cho phép bạn tạo cụm MongoDB hỗ trợ replication.
2. Thiết lập máy chủ MongoDB cục bộ với replication.

## Công nghệ sử dụng

- [Docker](https://docs.docker.com/get-docker/) (docker-compose)
- YAML
- Bash

## Cài đặt

Clone dự án

```bash
  $ git clone git@github.com:AlaeddineMessadi/Mongodb-Replica-Set-docker-compose.git mongodb-replset
```

Truy cập vào thư mục dự án

```bash
  $ cd mongodb-replset
```

Khởi động máy chủ

```bash
  $ ./start.sh
```

Nếu bạn không sử dụng script `./start.sh`, bạn cần chạy `$ docker exec mongo1 /scripts/init.sh` sau khi thực hiện lệnh `$ docker-compose up -d` để khởi tạo replica set trên các máy chủ.

Dừng máy chủ

```bash
  $ ./stop.sh

  # hoặc

  $ docker-compose down
```

## Đóng góp

Pull request luôn được chào đón. Đối với những thay đổi lớn, vui lòng mở một issue trước để thảo luận về những gì bạn muốn thay đổi.
