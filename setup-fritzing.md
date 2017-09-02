# Cài đặt phần mềm vẽ mạch Fritzing trên hệ điều hành Ubuntu 16.04

* **Thực hiện:** Thi Minh Nhựt - **Email:** thiminhnhut@gmail.com

* **Thời gian**: Ngày 02 tháng 09 năm 2017

## Nguồn tham khảo

* [Fritzing Download](http://fritzing.org/download/)

## Nội dung

* Tải [Fritzing](http://fritzing.org/download/) từ địa chỉ: http://fritzing.org/download/

* Giải nén file cài vừa tải về: ví dụ `fritzing-0.9.3b.linux.AMD64.tar.bz2` được thư mục `fritzing-0.9.3b.linux.AMD64`.

* Di chuyển thư mục `fritzing-0.9.3b.linux.AMD64` đến nơi chúng ta muốn cài đặt, ví dụ thư mục `/home/$USER/`:

    ```bash
    $ mv fritzing-0.9.3b.linux.AMD64 /home/$USER/
    ```
* Di chuyển đến thư mục `fritzing-0.9.3b.linux.AMD64`:

    ```bash
    $ cd /home/$USER/fritzing-0.9.3b.linux.AMD64
    $ sudo ./install_fritzing.sh
    ```

* Tạo shell thực thi `fritzing`:

    ```bash
    $ sudo nano /usr/local/bin/Fritzing
    ```

    + Thêm vào nội dung như sau:

    ```bash
    #!/bin/sh
    export FRITZING_HOME=/home/$USER/fritzing-0.9.3b.linux.AMD64
    $FRITZING_HOME/Fritzing $*
    ```

    + Mỗi lần muốn mở `Fritzing` chỉ cần gõ vào terminal lệnh `Fritzing`.

* Thêm icon `Fritzing` vào `Search Applications`:

    ```bash
    $ sudo mv fritzing.desktop /usr/share/applications/
    ```
