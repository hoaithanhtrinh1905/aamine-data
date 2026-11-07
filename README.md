# aamine-data

Gói dữ liệu **giới hạn tốc độ và camera** dùng offline cho các ứng dụng của AuraTech (Pet HUD, AAMine). / Offline speed-limit and speed-camera packs used by AuraTech apps.

## Giấy phép / License

- **Dữ liệu** trong các gói `*.aara` được dựng từ OpenStreetMap, © OpenStreetMap contributors, theo giấy phép **[ODbL 1.0](https://opendatacommons.org/licenses/odbl/1-0/)**. Gói là cơ sở dữ liệu dẫn xuất: phải ghi công OpenStreetMap và chia sẻ lại theo cùng giấy phép. / The packs are a database derived from OpenStreetMap data and are licensed under the **ODbL 1.0**; attribution is required.
- File [`LICENSE`](LICENSE) (MIT) chỉ áp dụng cho **mã và tài liệu** trong repo này, **không** áp dụng cho dữ liệu. / The MIT `LICENSE` covers code and documents only, **not** the data.

## Cách phát hành / Releases

Mỗi nước có hai loại release (mã nước 2 chữ, ví dụ `kr`):

| Tag | Nội dung |
| --- | --- |
| `kr-YYYYMMDD` | gói `kr.aara` + `kr-manifest.json` của bản dữ liệu đó |
| `kr-latest` | chỉ `kr-manifest.json`, trỏ tới bản mới nhất |

Ứng dụng đọc `…/releases/download/kr-latest/kr-manifest.json`, kiểm `format`, `size`, `sha256`, rồi tải `kr.aara` từ tag trong manifest. Không dùng `releases/latest` (chung cho cả repo).

## Định dạng `AARA` v1

Big-endian; toạ độ đơn vị 1e-5 độ; ô lưới 1000 đơn vị. Đặc tả đầy đủ nằm ở đầu file `build_pack.py` của ứng dụng dựng gói. Dữ liệu có thể không đúng, chỉ mang tính tham khảo. / Data may be wrong and is for reference only.
