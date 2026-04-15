[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574003&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** havietkhanh49@example.com
**Name:** Ha Viet Khanh

---

## Mo ta

Bai lab nay xay dung mot ETL pipeline don gian de doc du lieu tu `raw_data.json`, kiem tra chat luong, chuan hoa category, tinh gia giam 10%, va luu ket qua ra `processed_data.csv`. Ngoai ra, du an co them experiment report de mo ta tac dong cua du lieu sach va du lieu ban len mot agent mo phong.

Pipeline xu ly 3 buoc chinh: extract, validate, transform, load. Du lieu khong hop le se bi loai bo neu `price <= 0` hoac `category` rong. Du lieu hop le se duoc them `discounted_price` va `processed_at` de theo doi thoi diem xu ly.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
python generate_garbage.py
python agent_simulation.py
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

Pipeline da xu ly du lieu tu 5 records ban dau, giu lai 3 records hop le, loai bo 2 records khong hop le, va tao ra file CSV co cac cot `discounted_price` va `processed_at`. Khi chay agent voi clean data, ket qua on dinh va dung logic hon so voi garbage data. Dieu nay cho thay chat luong du lieu tac dong truc tiep den do chinh xac cua he thong.
