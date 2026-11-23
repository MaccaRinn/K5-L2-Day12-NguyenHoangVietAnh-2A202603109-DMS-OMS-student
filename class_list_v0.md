# Danh sach lop v0 - Nguyen Hoang Viet Anh · G02

## DMS (it nhat 6 lop)

| # | Lop / thuoc tinh | Gia tri | De lam gi (chuc nang DMS) | Nhìn thay duoc tren IR? |
|---|---|---|---|---|
| 1 | eye_state | open / closed / unknown | Phat hien buon ngu, nham mat lau va chu y tai xe | Co, tru khi mat bi che hoac phan xa |
| 2 | gaze_zone | road / mirror / cluster / center / lap / other | Xac dinh tai xe co nhin duong va phan tich su mat tap trung | Co mot phan neu huong dau va mat xac dinh ro |
| 3 | glasses | none / clear / sun / unknown | Tranh sai nhan mat va dieu chinh mo hinh theo tinh huong deo kinh | Co, nhung kinh ram co the gay unknown |
| 4 | hand | driver/passenger, left/right, on_wheel yes/no/unknown | Giam sat thao tac tay va nguy co sao nhang tai xe | Co neu tay du sang va hinh dang ro |
| 5 | phone | held / mounted / lap | Phat hien su dung dien thoai va canh bao phan tam | Co neu thay du hinh dang canh, goc hoac man hinh |
| 6 | face13 | 13 diem mat, occluded/outside | Theo doi cung va toa do dau de suy ra yaw/pitch va mat | Co voi NIR, co diem khong thay thi dung co co

## OMS (it nhat 6 lop)

| # | Lop / thuoc tinh | Gia tri | De lam gi (chuc nang OMS) | Nhìn thay duoc tren IR? |
|---|---|---|---|---|
| 1 | person | seat theo xe | Theo doi nguoi tren tung ghe va diem an toan | Co neu hinh dang nguoi du sang |
| 2 | child_seat | seat, occupied=no/unknown | Tu dong tich hop trang thai ghe va canh bao sai su dung | Co qua hinh dang ghe, khong chac thi unknown |
| 3 | infant_seat | seat, facing=rear/front | Khuyen nghi huong ghe va dieu khien tui khi | Co neu hinh dang ghe va huong ro |
| 4 | object | bag / box / cup / other, seat | Nhac nhat vat de tren ghe va tranh vat tro han che | Co neu hinh dang ro; mau khong duoc dung de nhan |
| 5 | seat | rear_left / rear_middle / rear_right | Lam nhan dien vi tri theo xe va lap chuc nang theo ghe | Co qua boi canh, khong thay doi theo ben trai anh |
| 6 | seatbelt | worn_correct / worn_incorrect / not_worn / unknown | Canh bao khong tha day va kiem tra thai do an toan | Co neu day du sang; tren SVIRO chi dung not_worn hoac unknown |

## 2 cau hoi leo thang

1. Cau hoi: Khi child_seat bi vat che mot phan, occupied nen la no hay unknown?
   Khung vi du: G02 S03.
   Ban tam gan the nao va vi sao: unknown neu khong thay ro ben trong; khong suy doan occupied=yes.
2. Cau hoi: Khi mat bi quay goc 90° va chi thay mot mat, co nen ve diem face13 cho mat bi che hay khong?
   Khung vi du: G02 D04.
   Ban tam gan the nao va vi sao: chi danh occluded/outside neu co the suy ra vi tri; khong ve cho đủ.
