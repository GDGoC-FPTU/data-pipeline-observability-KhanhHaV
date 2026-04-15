# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** AI20K-2026
**Name:** Khanh Ha
**Date:** 2026-04-15

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Agent: Based on my data, the best choice is Laptop at $1200. | 10 | Du lieu sach, category dung, price hop le, tra loi on dinh. |
| Garbage Data (`garbage_data.csv`) | Agent Error: I'm choking on the data! | 2 | File co duplicate IDs, wrong types, outliers, va null values. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Garbage data lam cho agent mat do tin cay cua du lieu dau vao. Khi co duplicate IDs, mo hinh co the dem lap mot san pham nhieu lan va nghi rang do la phan hoi pho bien. Wrong data types nhu chuoi thay vi so lam cho phep so sanh va sap xep bi loi hoac cho ket qua sai. Outliers co gia tri qua lon lam lech quyet dinh, khien agent uu tien mot mau bat thuong thay vi xu huong chung. Null values va category rong lam bo loc bi khoang trong, co the gay loi khi truy van hoac tra ve tap ket qua rong. Trong bai nay, clean data giup agent tra loi ro rang va 100% on dinh, trong khi garbage data lam qua trinh truy van bi voi, ket qua tro nen sai hoac bi crash. Dieu do cho thay chat luong du lieu la dieu kien tien quyet truoc khi toi uu prompt hay mo hinh.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** Dong y. Mot prompt tot chi co the khai thac thong tin co san, con du lieu kem chat luong se day agent vao loi logic, sai so sanh, va output khong on dinh. Voi du lieu sach, cung mot cau hoi don gian co the tra loi nhanh va chinh xac. Voi du lieu ban, ngay ca agent tot cung co the tra loi sai, do do cai thien du lieu dau vao thuong mang lai hieu qua lon hon viec chi sua prompt.
