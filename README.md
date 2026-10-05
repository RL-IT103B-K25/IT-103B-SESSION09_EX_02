Lỗi 1:

const basePrice = bookingReservation.priceKey;
priceKey là biến chứa "roomPrice" nên phải dùng:
const basePrice = bookingReservation[priceKey];

Lỗi 2:

bookingReservation.discountCode = undefined;
Cách này không xóa key, mà chỉ gán giá trị undefined cho key.

Phải dùng:
delete bookingReservation.discountCode;
→ Thuộc tính discountCode được xóa hoàn toàn khỏi object.

Lỗi 3:

bookingReservation.key
Trong vòng for...in, key là biến chứa tên thuộc tính, nên phải dùng:
bookingReservation[key]