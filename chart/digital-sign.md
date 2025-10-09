  
# Digital signature
Hướng dẫn sử dụng chức năng chữ ký số trên trang dịch vụ công (và các trang tương tự) trong lần đầu tiên sử dụng.
## Flowchart
Sơ đồ thiết lập chữ ký số.
  ```mermaid
  flowchart TD
  Login --> Install
  subgraph Login
    direction LR
    Access[Access dichvucong]
    Service[Select service]
    Token[Plug USB token]
    Access --> Service
    Service --> Token
  end
  subgraph Install[Install software]
    direction LR
    Plugin[Install plugin from USB] --> dotNet[Update dot Net framework]
  end
  subgraph Setup[Setup digital signature]
    Upload[Upload signature image] --> Serial[Get serial number]
    Serial --> Save[Save digital signature]
  end
  subgraph Sign
    direction LR
    Click[Click service to sign] --> Pass[Input token password]
  end
  Install --> Setup
  Setup --> Sign
  Sign --> Store([Store USB token])
```

## Guide
### Login
#### Access website
- Truy cập vào trang dịch vụ công của Cục Quản lý Dược (dichvucong.dav.gov) hoặc trang tương tự của Bộ y tế (dichvucong.moh.gov.vn).
- User: 0302560110
- Pass: liên hệ P. MKT/ P. NCPT/ P. ETC để share tài khoản công ty.
#### Select service
- Trên trang dịch vụ công sẽ có rất nhiều các thủ tục (dịch vụ) nộp hồ sơ trực tuyến trên nhiều lĩnh vực khác nhau (đăng ký thuốc, quảng cáo, công bố...)
- Chọn dịch vụ mong muốn bằng cách sử dụng công cụ tìm kiếm.
- Tạo hồ sơ theo hướng dẫn của website.
#### Plug USB token
- Cắm USB token vào máy tính.
- USB token là thiết bị phần cứng lưu chứng thư số phục vụ cho ký số. USB này công ty cần mua của các đơn vị cung cấp dịch vụ chữ ký số (Viettel, VNPT...) . Liên hệ P. CNTT, P. MKT, P. HCNS, P. CS ETC nếu chưa có USB token.
- Kiểm tra chứng thư số trong USB xem còn hạn hay không (clik vào USB).
### Install software
#### Install plugin
- Khi thao tác ký số, nếu thiếu plugin thì hệ thống sẽ tự hiển thị cảnh báo (alert) và tải về file cài plugin.
- Giải nén file cài, nhập pass 123456 (default pass) để giải nén.
- Cài plugin vào máy (reset máy tính nếu cần).

#### update dot Net framework
- Kiểm tra phiên bản dot Net framework trên máy tính có phải là phiên bản 4.5 (hoặc cao hơn) chưa.
- Nếu chưa tải file dot Net framework từ [Microsoft](https://www.microsoft.com/en-us/download/details.aspx?id=30653)
- Cài vào máy tính (reset máy tính nếu cần).
### Set up digital signature
Để có thể ký số, cần cài đặt chữ ký só vào web/ app dịch vụ công. Thao tác này chỉ làm 1 lần duy nhất, các lần sau hệ thống sẽ tự động sử dụng chữ ký số đã cài lần đầu.
- Truy cập vào mục `Cài đặt chữ kỹ số`
- Nhấn nút `Tạo mới chữ ky`
- Tải ảnh chữ ký.
- Nhấn nút lấy số `serial` (đảm bảo đang cắm USB token mới có thể lấy serial).
- Lưu chữ ký số đã tạo.
### Sign
- Chọn hồ sơ cần nộp trực tuyến (tạo mới nếu chưa có).
- Nhấn nút `Ký soos`.
- Nhập mật khẩu của USB token (liên hệ người bảo quản USB nếu chưa có).
- Ký số
- Nộp hồ sơ.
## Summary
Thao tác ký số sẽ tương tự nhau trên các nền tảng. Trong lần đầu tiên sử dụng có thể phải thao tác nhiều bước cài đặt/ cập nhật phần mềm điều khiển, thiết lập chữ ký số. Trong các lần sử dụng sau này, các bước thiết lập sẽ không cần thiết mà chỉ còn 2 bước chính là `Tạo hồ sơ` --> `Ký số` mà thôi.
